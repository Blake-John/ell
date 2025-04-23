# 01 gif to mp4

FFmpeg，一个强大的多媒体处理工具。以下是使用 FFmpeg 将 GIF 转换为 MP4 的具体步骤和命令：

在命令行中运行以下命令，将 GIF 文件转换为 MP4 视频：

```bash
ffmpeg -i input.gif -movflags faststart -pix_fmt yuv420p output.mp4
```

## 参数说明

- `-i input.gif`：指定输入的 GIF 文件。
- `-movflags faststart`：优化 MP4 文件，使其适合网络播放。
- `-pix_fmt yuv420p`：指定像素格式为 YUV420P，以确保兼容性。
- `output.mp4`：输出的 MP4 文件名。

## 示例

假设你有一个名为 `animation.gif` 的 GIF 文件，你可以将其转换为 MP4 文件 `animation.mp4`，命令如下：

```bash
ffmpeg -i animation.gif -movflags faststart -pix_fmt yuv420p animation.mp4
```

## 注意事项

- **文件路径**：确保输入的 GIF 文件路径正确。
- **输出文件**：转换后的 MP4 文件将保存在指定的输出路径中。
- **转换质量**：可以根据需要调整转换质量，例如通过添加 `-qscale:v 2` 参数来提高视频质量。

通过以上步骤，你可以使用 FFmpeg 将 GIF 文件成功转换为 MP4 格式的视频文件。