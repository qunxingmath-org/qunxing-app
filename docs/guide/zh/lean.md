[目录](README.md) · **Lean** · [English](../en/lean.md)

# Lean

## Lean 是什么，为什么要装

Lean 是一种能让电脑检查证明的语言。AI 写的自然语言证明可能有漏洞，Lean 检查过的证明就可靠得多。

**群星用 Lean 做两件事**：
1. **Lean 检查**：负责写 Lean 的 Agent 把证明写成 Lean，在你的电脑上编译。
   - 编译通过，而且只用了三条标准公理，才算"Lean 通过"。
2. **题意复核**：另一个 Agent 在全新的会话里核对 Lean 里写的命题是不是原题。
   - 防止"证明了一个更简单的题"。

两样都过，星图上的星才会点亮。

**不装 Lean 也能用**：可以解题、留下运行记录，但结果只能停在"解出"，到不了"Lean 通过"。

## 检查电脑上有没有 Lean

- 新手引导的 **Lean（可选）** 一步，点 **检查**；
- 或者在设置里重新进行新手引导，走到这一步。

![新手引导的 Lean 一步：没有找到 Lean，下面是安装步骤和"再检查一次"按钮](images/onboarding-lean.webp)

找到了，会显示 elan 和 Lean 的版本，以及 Mathlib 缓存是否可用。

## 安装

**新手引导的这一步会按你的系统给出具体命令**，照着做就行。在 Windows 上一般是这样：

1. **装 elan**。elan 是 Lean 的版本管理器，会自动装好需要的 Lean 版本。
   - 打开"命令提示符"，或 7.4.1 以上版本的 PowerShell，依次运行：

```powershell
curl -O --location https://elan.lean-lang.org/elan-init.ps1
powershell -ExecutionPolicy Bypass -f elan-init.ps1
del elan-init.ps1
```

2. **关掉终端，重新打开一个**，运行：

```powershell
lean --version
```

   能看到版本号就装好了。

3. **回到群星，点 再检查一次**。

安装命令以 elan 官方说明为准：<https://github.com/leanprover/elan>

## 第一次检查会比较慢

- 第一次做 Lean 检查时，群星会下载 Mathlib 的缓存。Mathlib 是 Lean 的数学库，缓存比较大。
- 之后的检查就快了。
- 编译时间和内存峰值会记在运行页的验证账本里。

## 结果页上的 Lean

结果页"对不对"一栏会写清楚：

| 写的是 | 意思 |
|---|---|
| Lean 在本机编译通过 · 只用了标准公理 | 通过 |
| Lean 编译通过，但用了标准以外的公理 | 不算通过，会列出用了哪些公理 |
| Lean 没通过 | 编译失败。失败的记录照样保存 |

结果页的"本地文件"里，可以找到 Lean 工程的文件夹。

## 题面锁定

**群星题库里的一部分题，已经有维护者审核锁定的 Lean 题面**：
- 用锁定的题面，题意复核可以直接复用题卡上已有的复核。

**没有锁定题面的题**：
- Lean 证明的是本次运行自己写的题面；
- 星上会带"题面未锁定"的记号；
- 不计入网站的"已解决"数，等维护者锁定后才算。

下一步：[研究计划](research-plans.md)
