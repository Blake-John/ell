[MinerU](https://mineru.readthedocs.io/zh-cn/latest/index.html) 是一个在 [书生·浦语](https://github.com/InternLM/InternLM) 模型开发中诞生的，它能够解决科技文献中符号转化的问题，最主要的便是能够提取 PDF 文件为 Markdown 文件。这种转换基于大模型，因此，我们也需要配置一个能够让模型本地部署的环境。

# Installation

MinerU 的安装及其简单，支持在 Windows/Linux 系统上运行，但暂时不支持 ARM 结构。该工具的部署基于 Anaconda 进行安装，且十分便捷。

## 创建环境

我们在 Anaconda 中创建一个专门的环境供 MinerU 使用 :

```bash
conda create -n MinerU python=3.10
```

> MinerU 要求在 conda 环境下使用 `python 3.10` 来运行

接下来，就可以安装 MinerU 的工具 : 

```bash
conda activate MinerU
pip install -U magic-pdf[full] --extra-index-url https://wheels.myhloli.com -i https://mirrors.aliyun.com/pypi/simple
```

我们可以通过 `magic-pdf --version` 来检查安装是否成功。

## 下载模型

MinerU 基于模型进行识别，因此，我们还需要下载相应的模型，我们可以通过 Hugging Face 或者 ModelScope 来下载。

### Hugging Face

```bash
pip install huggingface_hub
wget https://gcore.jsdelivr.net/gh/opendatalab/MinerU@master/scripts/download_models_hf.py -O download_models_hf.py
python download_models_hf.py
```

> 并不推荐使用该方法，因为没有较好的网络环境

### ModelScope

```bash
pip install modelscope
wget https://gcore.jsdelivr.net/gh/opendatalab/MinerU@master/scripts/download_models.py -O download_models.py
python download_models.py
```

推荐在 ModelScope 中下载该模型，较为快捷方便。

python脚本会自动下载模型文件并配置好配置文件中的模型目录

配置文件可以在用户目录中找到，文件名为 `magic-pdf.json` ，该文件存放于用户的 **家目录**  中

## 更新模型

再次运行脚本即可。

# Usage

该工具提供了命令行工具 `magic-pdf` 让我们使用，其用法如下 : 

```text
magic-pdf --help
Usage: magic-pdf [OPTIONS]

Options:
  -v, --version                display the version and exit
  -p, --path PATH              local pdf filepath or directory  [required]
  -o, --output-dir PATH        output local directory  [required]
  -m, --method [ocr|txt|auto]  the method for parsing pdf. ocr: using ocr
                               technique to extract information from pdf. txt:
                               suitable for the text-based pdf only and
                               outperform ocr. auto: automatically choose the
                               best method for parsing pdf from ocr and txt.
                               without method specified, auto will be used by
                               default.
  -l, --lang TEXT              Input the languages in the pdf (if known) to
                               improve OCR accuracy.  Optional. You should
                               input "Abbreviation" with language form url: ht
                               tps://paddlepaddle.github.io/PaddleOCR/en/ppocr
                               /blog/multi_languages.html#5-support-languages-
                               and-abbreviations
  -d, --debug BOOLEAN          Enables detailed debugging information during
                               the execution of the CLI commands.
  -s, --start INTEGER          The starting page for PDF parsing, beginning
                               from 0.
  -e, --end INTEGER            The ending page for PDF parsing, beginning from
                               0.
  --help                       Show this message and exit.


## show version
magic-pdf -v

## command line example
magic-pdf -p {some_pdf} -o {some_output_dir} -m auto
```

其中 : 

- `-p` - 可以指定 **某个文件**，也可以指定 **某一目录**，实现目录下 pdf 的全转换
- `-o` - 用于指定输出文件的目录

因此，我们可以通过以下命令来转换 pdf : 

```bash
magic-pdf -p <file_or_path_to_pdf> -o <output_dir>
magic-pdf -p test.pdf -o test/
```

这样，就能够讲 pdf 转化为 md 文件，其输出的目录结构如下 : 

```text
output_dir/
├── some_pdf.md                          # markdown 文件
├── images/                              # 存放图片目录
├── some_pdf_layout.pdf                  # layout 绘图 （包含layout阅读顺序）
├── some_pdf_middle.json                 # minerU 中间处理结果
├── some_pdf_model.json                  # 模型推理结果
├── some_pdf_origin.pdf                  # 原 pdf 文件
├── some_pdf_spans.pdf                   # 最小粒度的bbox位置信息绘图
└── some_pdf_content_list.json           # 按阅读顺序排列的富文本json
```

最重要的便是 `some_pdf.md` 文件以及 `images/` 目录，保存了我们的转化结果。

# CUDA 加速

## 环境配置

### CUDA cuDNN

我们也可以使用 CUDA 来加速转化过程，但是，环境要求较为严格 : 

- **CUDA 11.8** - [https://developer.nvidia.com/cuda-11-8-0-download-archive](https://developer.nvidia.com/cuda-11-8-0-download-archive) 
- **cuDNN v8.7.0 (November 28th, 2022), for CUDA 11.x** - [https://developer.nvidia.com/rdp/cudnn-archive](https://developer.nvidia.com/rdp/cudnn-archive) 

### torch torchvision

我们应该安装支持 cuda 的 `torch` 和 `torchvision` ，若是遇到网速问题，我们也可以自己到官方[下载地址](https://download.pytorch.org/whl/cu118) 下载 `whl` 来安装 : 

#### pip

```bash
pip install --force-reinstall torch==2.3.1 torchvision==0.18.1 --index-url https://download.pytorch.org/whl/cu118
```

#### whl

一般情况下，我们选择 `cp310` 版本，下载完 `whl` 文件后，切到目标所在目录，直接 : 

```bash
pip install --force-reinstall ./torch-2.3.1+cu118-cp310-cp310-win_amd64.whl
pip install --force-reinstall ./torchvision-0.18.1+cu118-cp310-cp310-win_amd64
```

## 修改配置文件

我们上面提到， `magic-pdf.json` 中保存了配置信息，接下来，我们应该修改配置使得其能够使用 CUDA 进行推理加速 : 

```json
{
  "device-mode":"cuda"
}
```

做完以上这些，我们就可以享受 GPU 带来的加速，

> [!tip] 
> CUDA 加速是否生效可以根据 log 中输出的各个阶段的耗时来简单判断，通常情况下， `layout detection time` 和 `mfr time` 应提速10倍以上。

