# Openclaw Skills Sally Xie

## English

This repository contains reusable OpenClaw skills for end users and bot builders.

### Included Skills

#### `openclaw-immediate-ack`

This skill adds an immediate acknowledgement reply for Feishu and DingTalk.

Its purpose is to let users quickly know that:

- the message was sent successfully
- the bot received it successfully
- processing has already started

It supports:

- Feishu
- DingTalk
- bilingual guidance
- acknowledgement replies that follow the current conversation language

Install from Terminal:

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo sallyxie2026/Openclaw_skills_sallyxie --path openclaw-immediate-ack
```

Install by talking to OpenClaw:

```text
Please help me install the skill openclaw-immediate-ack from the GitHub repo sallyxie2026/Openclaw_skills_sallyxie.
```

Or:

```text
Please use the skill installer to install openclaw-immediate-ack from sallyxie2026/Openclaw_skills_sallyxie.
```

#### `video-to-gif`

This skill converts a local video clip into a GIF using `ffmpeg`.

It supports:

- custom frame rate
- custom width
- custom start time
- custom duration
- bilingual skill guidance

Install from Terminal:

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo sallyxie2026/Openclaw_skills_sallyxie --path video-to-gif
```

Install by talking to OpenClaw:

```text
Please help me install the skill video-to-gif from the GitHub repo sallyxie2026/Openclaw_skills_sallyxie.
```

Or:

```text
Please use the skill installer to install video-to-gif from sallyxie2026/Openclaw_skills_sallyxie.
```

### After Installation

After installing a new skill, restart Codex/OpenClaw so the skill can be loaded correctly.

## 中文

这个仓库收录了一些可复用的 OpenClaw skills，适合普通用户和机器人搭建者使用。

### 当前包含的 Skills

#### `openclaw-immediate-ack`

这个 Skills 的作用是让 OpenClaw 机器人在飞书和钉钉里收到消息后，先立即回复一句简短确认。

它可以让用户快速知道：

- 消息已经成功发出
- 机器人已经成功接收
- 后续处理已经开始

它支持：

- 飞书
- 钉钉
- 中英双语说明
- 即时确认自动跟随当前对话语言

在终端里安装：

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo sallyxie2026/Openclaw_skills_sallyxie --path openclaw-immediate-ack
```

直接和 OpenClaw 对话安装：

```text
请帮我从 GitHub 仓库 sallyxie2026/Openclaw_skills_sallyxie 安装 openclaw-immediate-ack 这个 skill。
```

或者：

```text
请使用 skill installer，从 sallyxie2026/Openclaw_skills_sallyxie 安装 openclaw-immediate-ack。
```

#### `video-to-gif`

这个 Skills 的作用是使用 `ffmpeg` 将本地视频片段转换成 GIF。

它支持：

- 自定义帧率
- 自定义宽度
- 自定义开始时间
- 自定义时长
- 中英双语说明

在终端里安装：

```bash
python3 "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo sallyxie2026/Openclaw_skills_sallyxie --path video-to-gif
```

直接和 OpenClaw 对话安装：

```text
请帮我从 GitHub 仓库 sallyxie2026/Openclaw_skills_sallyxie 安装 video-to-gif 这个 skill。
```

或者：

```text
请使用 skill installer，从 sallyxie2026/Openclaw_skills_sallyxie 安装 video-to-gif。
```

### 安装后说明

安装完成后，请重启 Codex/OpenClaw，让新的 skill 被正确加载。
