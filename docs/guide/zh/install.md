[目录](README.md) · **安装** · [English](../en/install.md)

# 安装

## 需要什么

- **系统**：Windows 10 或 11，64 位。macOS 版在做。
- **AI 工具**：至少一个会写代码的 AI 工具，并且已经登录：
  - Codex CLI；
  - Claude Code；
  - Gemini CLI。
  - 用订阅或 API 都行。
- **Lean 4**：可选。要让结果过 Lean 检查才需要，见 [Lean](lean.md)。
- **联网**：更新题库、查新、调用 AI 时要联网。

## 下载

两种都行，内容一样：

| 文件 | 适合谁 |
|---|---|
| [安装包 `Qunxing-Setup.exe`](https://github.com/qunxingmath-org/qunxing-app/releases/latest/download/Qunxing-Setup.exe) | 大多数人 |
| [完整应用包 `Qunxing-Windows-x64.zip`](https://github.com/qunxingmath-org/qunxing-app/releases/latest/download/Qunxing-Windows-x64.zip) | 不想安装的；用单位电脑的；想放在 U 盘里带走的 |

- GitHub 下载慢的话，用[网站下载页](https://www.qunxingmath.org/download/)上的国内镜像。文件和 GitHub 上的一样。
- 所有版本和版本说明：<https://github.com/qunxingmath-org/qunxing-app/releases>

## 用安装包

1. 双击 `Qunxing-Setup.exe`。
2. 按提示点下一步。
   - 装在当前用户目录下，**不需要管理员权限**。
   - 会建开始菜单和桌面快捷方式。
3. 电脑上没有 WebView2 运行库的话，安装程序会先告诉你，再从微软官网下载安装。
   - WebView2 是微软的组件，用来显示群星的界面。
   - Windows 11 自带；Windows 10 大多也已经装了。
4. 装好以后，从开始菜单打开"群星"。

## 用完整应用包

1. 右键 zip → **全部解压缩**，解压到任意文件夹，例如 `D:\Qunxing`。
   - 不要在压缩包里直接双击运行。
2. 双击解压出来的 `Qunxing.exe`。

## Windows 提示"Windows 已保护你的电脑"

还没有代码签名的版本、刚发布的新版本，都可能出现这个提示。

1. 先确认文件来源：本仓库的 Release，或者群星网站。
2. 点 **更多信息**，再点 **仍要运行**。

我们在申请免费的开源代码签名。签了名，这个提示会少很多；但新版本刚发布时，仍可能出现一段时间。微软要按下载量慢慢积累信誉。

## 核对文件（可选）

想确认下载的文件没被改过：

1. 在下载文件夹的空白处点右键，选"在终端中打开"。Windows 10 要按住 Shift 再点右键，选"在此处打开 PowerShell 窗口"。
2. 运行：

```powershell
Get-FileHash .\Qunxing-Setup.exe -Algorithm SHA256
```

3. 把结果和 Release 里 `SHA256SUMS.txt` 的对应一行比一比，应该完全一样。
   - 网站下载页上也列出了每个文件的 SHA-256。

## 更新

- **有新版本时，群星会提示你**。提示里的"下载"会打开网站下载页。
- **怎么提示，在设置里改**：设置 → **更新与联网** → **收到更新时**，三选一：
  - **自动更新**；
  - **先问我**（默认）；
  - **不接收**。
- **怎么装新版**：
  - 安装版：下载新的安装包，直接运行，覆盖安装。
  - 免安装版：解压到新文件夹，用新的 `Qunxing.exe`。
- **你的运行记录不受影响**：它们在数据文件夹里，不在程序文件夹里。见[卸载与数据位置](uninstall.md)。

下一步：[第一次打开](first-run.md)
