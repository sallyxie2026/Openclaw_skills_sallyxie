---
name: video-to-srt
description: Generate timecoded SRT subtitles from local video or audio files. Use when a user wants a local low-cost subtitle workflow, asks to transcribe local media into SRT with timestamps, or needs subtitle files that can be imported into editing tools. Includes bilingual Chinese-English guidance.
---

# Video to SRT / 视频转 SRT

## Purpose / 功能定位

### English

Use this skill when the task is to convert a local video or audio file into a timecoded `SRT` subtitle file.

This skill is intended for requests such as:

- convert local video to subtitles
- transcribe audio into SRT
- generate subtitle files for editing tools
- create low-cost local subtitles without a cloud transcription workflow

### 中文

当任务是把本地视频或音频文件转换成带时间轴的 `SRT` 字幕文件时，应使用这个 Skills。

这个 Skills 适合处理以下类型的请求：

- 把本地视频转成字幕
- 把音频转成 `SRT`
- 为剪辑软件生成字幕文件
- 希望走本地低成本字幕流程，而不是云端转写流程

## Workflow / 工作流程

### English

1. Create a new top-level task folder for the request in the workspace.
2. Locate the user's local media file and confirm the language choice only if it is unclear.
3. Run `scripts/run_local_subtitles.sh` from this skill folder.
4. Default to `--language auto` and `--model small`. Use `--language zh` when the media is clearly Chinese. Switch to `--model medium` only when the user wants better accuracy and accepts slower runtime.
5. Inspect the generated `.srt` file by checking the first and last few cues before handing it off.
6. Return the subtitle path and mention that editors which accept `SRT`, including Jianying desktop, can import it.

### 中文

1. 在工作区中为当前请求创建一个新的顶层任务目录。
2. 找到用户的本地媒体文件。只有当语言不明确时，才额外确认语言。
3. 从这个 skill 目录运行 `scripts/run_local_subtitles.sh`。
4. 默认使用 `--language auto` 和 `--model small`。如果素材明确是中文，可改用 `--language zh`。只有当用户明确要更高准确率并接受更慢速度时，再切到 `--model medium`。
5. 交付前检查生成的 `.srt` 文件，至少查看开头和结尾几个字幕块。
6. 返回字幕文件路径，并说明支持 `SRT` 导入的编辑器都可使用它，包括剪映桌面版。

## Stable Defaults / 稳定默认值

### English

- Keep dependency installation inside a local virtual environment created by `scripts/run_local_subtitles.sh`.
- Keep caches local to the skill folder. This avoids macOS cache permission issues.
- Keep `HF_HUB_DISABLE_XET=1` enabled. This avoids a common Hugging Face Xet download failure.
- Prefer `SRT`. It is the simplest subtitle format for broad editor compatibility.
- Override `VENV_DIR`, `HF_HOME`, or `XDG_CACHE_HOME` only when reusing an existing environment or model cache is helpful.

### 中文

- 依赖安装默认放在 `scripts/run_local_subtitles.sh` 创建的本地虚拟环境里。
- 缓存默认保存在 skill 目录下，避免 macOS 的缓存权限问题。
- 保持 `HF_HUB_DISABLE_XET=1` 开启，规避常见的 Hugging Face Xet 下载失败问题。
- 默认优先使用 `SRT`，它是兼容面最广、最容易导入编辑器的字幕格式。
- 只有在确实要复用现有环境或模型缓存时，才覆写 `VENV_DIR`、`HF_HOME` 或 `XDG_CACHE_HOME`。

## Commands / 命令

Use the wrapper script for the normal path:

```bash
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --output-dir "/absolute/path/to/task/output" --copy-next-to-input
```

Use these common variants:

```bash
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --language auto --output-dir "/absolute/path/to/task/output" --copy-next-to-input
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --model medium --output-dir "/absolute/path/to/task/output" --copy-next-to-input
```

### 中文补充

常规路径请使用包装脚本：

```bash
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --output-dir "/absolute/path/to/task/output" --copy-next-to-input
```

常见变体：

```bash
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --language auto --output-dir "/absolute/path/to/task/output" --copy-next-to-input
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --language zh --output-dir "/absolute/path/to/task/output" --copy-next-to-input
scripts/run_local_subtitles.sh "/absolute/path/to/video.mp4" --model medium --output-dir "/absolute/path/to/task/output" --copy-next-to-input
```

## Validation / 校验

### English

- If the wrapper needs to install packages or download a model, request permission when required by the environment.
- Confirm that the final `.srt` exists.
- Preview the first and last cues with `sed -n '1,24p'` and `tail -n 24`.
- If the user wants a faster import workflow, keep a copy beside the source media with `--copy-next-to-input`.

### 中文

- 如果包装脚本需要安装依赖或下载模型，在当前环境要求时应先请求授权。
- 确认最终的 `.srt` 文件确实生成成功。
- 用 `sed -n '1,24p'` 和 `tail -n 24` 预览开头和结尾字幕块。
- 如果用户希望更方便地导入编辑器，可以用 `--copy-next-to-input` 在源文件旁边保留一份副本。

## Resources / 资源

- `scripts/run_local_subtitles.sh`: create or reuse a local virtual environment, install dependencies, configure stable cache paths, and run transcription.
- `scripts/transcribe_to_srt.py`: transcribe media and write timecoded SRT output.
- `scripts/requirements.txt`: minimal dependency list for the workflow.

### 中文补充

- `scripts/run_local_subtitles.sh`：创建或复用本地虚拟环境，安装依赖，配置稳定缓存目录，并执行转写。
- `scripts/transcribe_to_srt.py`：负责转写媒体并输出带时间轴的 `SRT` 文件。
- `scripts/requirements.txt`：这个流程需要的最小依赖列表。
