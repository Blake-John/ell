想要在 ROS 中使用外部 Python 的包，有如下几种做法，可参见 [官方文档](https://docs.ros.org/en/humble/How-To-Guides/Using-Python-Packages.html) 。

# 01 Via `rosdep`

我们可以通过 `rosdep` 来安装 `package.xml` 中所需要的包，因此，我们可以将需要的包写入 `package.xml` 中，并通过 : 

```bash
rosdep install -yr ./path/to/your/workspace
```

来安装 [Keywords](https://github.com/ros/rosdistro/blob/master/rosdep/python.yaml) 中给出的包。

> [!attention] 
> 通过 rosdep 安装的包 **实际上是通过系统包管理器** 来安装的包，因此只能从 keywords 中安装，详细的使用说明可见 [Rosdep](https://docs.ros.org/en/humble/Tutorials/Intermediate/Rosdep.html) 

# 02 Via System Package Manager

直接在系统中安装我们需要的包，优点是安装方便简单，且 **不会有依赖问题**（对于 Ubuntu 而言），缺点是可供安装的包并不全面，而且限定版本，对于我们需要的特定版本来说 **存在依赖问题**。

# 03 Via Virtual Environment

## 3.1 virtualenv

首先创建一个工作空间 : 

```bash
mkdir -p ~/colcon_venv/src
cd ~/colcon_venv/
```

然后在这个工作空间中创建需要的虚拟环境，并添加 `COLCON_IGNORE` : 

```bash
# Make a virtual env and activate it
virtualenv -p python3 ./venv
source ./venv/bin/activate

# Make sure that colcon does not try to build the venv
touch ./venv/COLCON_IGNORE
```

然后就可以在这个空间中安装你想要的软件包了 : 

```bash
python3 -m pip install gtsam pyserial
```

最后编译并运行

```bash
# Source Humble and build
source /opt/ros/humble/setup.bash
colcon build
```

## 3.2 conda #bug 

### 3.2.1 Solution1

1. 准备 Conda 环境

```bash
conda create -n your_environment_name python=3.12.3
conda activate your_environment_name
pip install rospkg
pip install -U colcon-common-extensions
```

利用以上步骤创建并激活虚拟环境，安装ROS2 运行的必要包

2. 利用 `colcon` 编译

确保虚拟环境已经激活

```bash
python -m colcon build
```

在通常的编译命令前加上 `python -m` 以 **使用虚拟环境中的 `colcon` 进行编译**

3. 运行程序

与常规运行ros包一样，运行编译好的包

```bash
source install/setup.bashrc
ros2 run your_package your_nodes
```

