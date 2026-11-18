# Dew ChatGPT/Codex Pet 安装包

这是“Dew”的完整 8×11 自定义 Pet 包，可供 ChatGPT/Codex 桌面端和兼容的 Codex CLI 使用；在兼容的 Dot/Pets 桌面界面中也可沿用这个角色包。仅允许非商业使用。

## 一键安装

如果已经使用 Windows 独立版，右键点击 Dew，选择“安装到 Codex”，等待完成提示即可。随后在客户端的 **设置 > Pets（宠物）** 中刷新并选择“Dew”；此后可以退出 Windows 独立版。

仅下载了本 Pet 安装包时，在本目录打开 PowerShell：

```powershell
powershell -ExecutionPolicy Bypass -File .\install-codex-pet.ps1
```

安装器只会把 `pet.json` 与 `spritesheet.webp` 复制到 `%CODEX_HOME%\pets\dew`；如果未设置 `CODEX_HOME`，则使用 `%USERPROFILE%\.codex\pets\dew`。它不需要管理员权限，不写注册表，也不访问网络。

原版深深使用同一根目录下的 `pets/shenshen`，可以和 `pets/dew` 同时保留。若旧版 Dew 安装器已经覆盖原版，先用新版脚本安装 Dew，再用原版安装包恢复深深并刷新 Pets 列表。

## ChatGPT/Codex 桌面端

安装后打开 **设置 > Pets**，选择 **Refresh** 和“Dew”，点击 **显示宠物 / 唤醒虚拟宠物**，或输入 `/pet`。在 Windows 上，默认快捷键 `Windows+Alt+P` 可显示悬浮控件并聚焦快捷对话。

## Dot/Pets 桌面外观

在支持自定义 Pet 的 Dot 界面中，可从形象列表选择 Dew。在已支持外观互通的账号中，Codex Pet 与 Dot 的形象可以互相选择，网页端也能同步使用；列表已有“Dew”时直接选择，无需重复安装或上传。

Dew 提供外观与动画，Dot 的任务、语音和插件能力由 OpenAI 客户端及服务提供。上述互通与网页同步以当前界面表现为依据；官方 Pets 文档仍将桌面自定义 Pet 描述为本地保存，因此请以客户端版本、账号和工作区实际提供的列表为准。

当前用法见 [OpenAI Pets 文档](https://learn.chatgpt.com/docs/pets)；Dot 的能力与可用条件见 [Meet dots](https://learn.chatgpt.com/docs/dots)。

## Codex CLI

在交互式 CLI 中输入 `/pets` 打开选择器，或输入 `/pets dew` 直接选择；使用 `/pets off` 关闭。终端必须支持 iTerm2 3.6+、Kitty graphics 或 Sixel，且不能位于 tmux/Zellij 内。

## 手动安装

将 `dew` 整个文件夹复制到：

```text
%USERPROFILE%\.codex\pets\dew
```

目录内必须保留 `pet.json` 和 `spritesheet.webp`。如果网页端尚未出现共享形象，可从 GitHub Release 下载单独的 `Shenshen-ChatGPT-Web-Pet.webp` 手动上传；不要将本安装包的 8×11 文件用于要求 8×9 图片的 Web 上传入口。

本项目非 DeepSeek 或 OpenAI 官方产品。视觉素材许可、来源和 AI 制作说明见随包提供的 `ASSET_LICENSE.md`、`LEGAL_NOTICE.md` 与 `AI_PROVENANCE.md`。
