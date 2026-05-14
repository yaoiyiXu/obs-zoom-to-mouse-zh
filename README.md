# OBS Zoom to Mouse 中文版

这是一个 OBS Lua 脚本，用于将选中的显示器采集源放大，并让画面聚焦到鼠标所在位置。

本仓库基于 [BlankSourceCode/obs-zoom-to-mouse](https://github.com/BlankSourceCode/obs-zoom-to-mouse) 修改整理，当前版本主要面向中文用户使用。

## 主要变化

- 将 OBS 脚本界面、按钮、选项说明和热键名称改为中文。
- 保留原脚本的鼠标位置放大、自动跟随、手动显示器参数、远程鼠标监听等能力。
- 在个人使用场景中做了兼容性和默认参数调整。

## 功能

- 对显示器采集源进行鼠标位置放大。
- 支持平滑放大和缩小动画。
- 支持放大后自动跟随鼠标。
- 支持鼠标移出采集源范围时继续跟随。
- 支持手动设置源位置、缩放比例和显示器分辨率。
- 支持通过 UDP 接收远程鼠标位置。
- 支持 OBS 前端热键：
  - 切换鼠标位置放大
  - 放大时切换鼠标跟随

## 安装

1. 下载 `obs-zoom-to-mouse-zh.lua`。
2. 打开 OBS。
3. 进入 `工具` -> `脚本`。
4. 点击 `+`，选择 `obs-zoom-to-mouse-zh.lua`。
5. 在脚本设置中选择要放大的显示器采集源。
6. 在 OBS 的 `设置` -> `热键` 中设置放大和跟随快捷键。

## 使用建议

- 推荐选择 OBS 的显示器采集源作为放大源。
- 如果选择的不是显示器采集源，请启用手动源位置设置，并填写源位置、缩放比例和显示器分辨率。
- 如果画面已经添加裁剪/填充滤镜，请优先使用非相对裁剪参数。
- 如果放大位置不准确，可以打开诊断日志，并检查显示器分辨率、源位置和缩放比例。

## 远程鼠标监听

如果 OBS 环境中可用 `ljsocket`，脚本设置里会显示远程鼠标监听选项。启用后，脚本会监听 UDP 数据包，用于接收远程客户端发送的鼠标坐标。

远程客户端可参考上游相关项目：

- [BlankSourceCode/obs-zoom-to-mouse-remote](https://github.com/BlankSourceCode/obs-zoom-to-mouse-remote)

## 来源与版权

原始项目：

- [BlankSourceCode/obs-zoom-to-mouse](https://github.com/BlankSourceCode/obs-zoom-to-mouse)

原始脚本文件头部声明：

```text
Copyright (c) BlankSourceCode. All rights reserved.
```

本仓库保留原作者署名和原始版权声明。本仓库中的修改主要包括中文界面、本地化说明和个人使用场景下的调整。

上游仓库当前未声明明确的开源许可证，因此本仓库不额外添加新的开源许可证。使用、复制、分发或二次修改前，请自行确认你拥有相应授权。

## 文件

- `obs-zoom-to-mouse-zh.lua`：中文界面版本脚本。
- `NOTICE.md`：来源、修改说明和版权提示。

