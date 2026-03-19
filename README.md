# OpenClaw Skills Sally Xie

Reusable public OpenClaw skills for local automation, subtitle generation, and Feishu or DingTalk bot workflows.

GitHub repository:

- https://github.com/sallyxie2026/Openclaw_skills_sallyxie

## English

This repository contains reusable OpenClaw skills.

### Included Skills

#### `openclaw-immediate-ack`

Adds an immediate acknowledgement reply for Feishu and DingTalk, so users can quickly tell that:

- the message was sent successfully
- the bot received it successfully
- processing has already started

Highlights:

- supports Feishu
- supports DingTalk
- bilingual skill guidance
- acknowledgement replies follow the active conversation language

#### `video-to-gif`

Converts a local video clip into a GIF with `ffmpeg`.

Highlights:

- supports custom frame rate
- supports custom width
- supports custom start time
- supports custom duration
- bilingual skill guidance

#### `video-to-srt`

Converts a local video or audio file into a timecoded `SRT` subtitle file.

Highlights:

- local low-cost subtitle workflow
- outputs standard `SRT`
- suitable for editors that support subtitle import
- supports language selection
- supports larger models when higher accuracy is needed
- bilingual skill guidance

## 中文

这个仓库收录了一些可复用的 OpenClaw skills。

### 当前包含的 Skills

#### `openclaw-immediate-ack`

这个 Skills 会给飞书和钉钉机器人增加“即时确认回复”能力，让用户快速知道：

- 消息已经成功发出
- 机器人已经成功接收
- 后续处理已经开始

特点：

- 支持飞书
- 支持钉钉
- 提供中英双语说明
- 即时确认会自动跟随当前对话语言

#### `video-to-gif`

这个 Skills 使用 `ffmpeg` 将本地视频片段转换成 GIF。

特点：

- 支持自定义帧率
- 支持自定义宽度
- 支持自定义开始时间
- 支持自定义时长
- 提供中英双语说明

#### `video-to-srt`

这个 Skills 可以把本地视频或音频文件转换成带时间轴的 `SRT` 字幕文件。

特点：

- 本地低成本字幕方案
- 输出标准 `SRT`
- 适合导入支持字幕文件的编辑工具
- 支持语言选择
- 需要更高准确率时可切换更大模型
- 提供中英双语说明
