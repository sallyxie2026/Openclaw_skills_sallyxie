# Openclaw Skills Sally Xie

## English

This repository contains reusable OpenClaw skills for end users and bot builders.

### Included Skill

- `openclaw-immediate-ack`

This skill adds an immediate acknowledgement reply for Feishu and DingTalk, so users can quickly see that:

- the message was sent successfully
- the bot received it successfully
- processing has already started

### Quick Install

There are two easy ways to install this skill.

#### Option 1: Install from Terminal

Open your Terminal app, then copy and paste the full command below and press Enter:

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo sallyxie2026/Openclaw_skills_sallyxie --path openclaw-immediate-ack
```

If you prefer the wrapped multi-line version, copy the whole block exactly as-is:

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo sallyxie2026/Openclaw_skills_sallyxie \
  --path openclaw-immediate-ack
```

After installation, restart Codex/OpenClaw so the new skill is loaded.

#### Option 2: Ask OpenClaw to install it for you

If you are already chatting with OpenClaw, you can ask it directly to install this skill from this GitHub repository.

You can send a message like:

```text
Please install the skill openclaw-immediate-ack from the GitHub repo sallyxie2026/Openclaw_skills_sallyxie.
```

Or:

```text
Please use the skill installer to install openclaw-immediate-ack from sallyxie2026/Openclaw_skills_sallyxie.
```

If you are talking to OpenClaw through Feishu or DingTalk, you can send the same request there. After installation, ask OpenClaw to restart or reload the environment if needed.

### Features

- Supports both Feishu and DingTalk
- Sends a short acknowledgement before the main reply starts
- Provides bilingual skill guidance
- Follows the active conversation language
  - Chinese conversation -> Chinese acknowledgement
  - English conversation -> English acknowledgement

## 中文

这个仓库收录了一些可复用的 OpenClaw skills，适合普通用户和机器人搭建者使用。

### 当前包含的 Skills

- `openclaw-immediate-ack`

这个 Skills 的作用是让 OpenClaw 机器人在飞书和钉钉里收到消息后，先立即回复一句简短确认，让用户快速知道：

- 消息已经成功发出
- 机器人已经成功接收
- 后续处理已经开始

### 一键安装

这个 skills 提供两种适合新手的安装方式。

#### 方式 1：在终端里安装

先打开终端（Terminal），然后把下面这一整行完整复制进去，直接按回车即可：

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo sallyxie2026/Openclaw_skills_sallyxie --path openclaw-immediate-ack
```

如果你更习惯看换行版，也可以复制下面这一整段，效果是一样的：

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo sallyxie2026/Openclaw_skills_sallyxie \
  --path openclaw-immediate-ack
```

你真正需要粘贴到终端里的，就是上面代码块里的命令本身，不需要额外加别的内容。

安装完成后，请重启 Codex/OpenClaw，让新的 skill 被正确加载。

#### 方式 2：直接和 OpenClaw 对话，让它帮你安装

如果你已经可以直接和 OpenClaw 对话，也可以不用自己敲终端命令，而是直接对它说：

```text
请帮我从 GitHub 仓库 sallyxie2026/Openclaw_skills_sallyxie 安装 openclaw-immediate-ack 这个 skill。
```

或者说得更明确一点：

```text
请使用 skill installer，从 sallyxie2026/Openclaw_skills_sallyxie 安装 openclaw-immediate-ack。
```

如果你是在飞书或钉钉里和 OpenClaw 对话，也可以直接发送上面这句话，让它帮你完成安装。

安装完成后，记得让 OpenClaw 重启，或者重新进入一次会话，让新 skill 生效。

### 功能特点

- 同时支持飞书和钉钉
- 在主回复开始前先发送一条即时确认
- Skills 内容为中英双语
- 即时确认会自动跟随当前对话语言
  - 中文对话 -> 输出中文确认
  - 英文对话 -> 输出英文确认
