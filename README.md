# <span style="color:orange">本说明文件分为<u>英文</u>和<u>中文</u>两部分</span>

---

# Real-Time Japanese Subtitle Transcription System (with Keyword Feature)

## 🧩 Introduction

This program is a **multi-language real-time speech transcription and translation system** based on the GPT-4o API. It features a modern and user-friendly graphical interface. Simply connect a microphone and click “Start Recording” to transcribe Japanese (or other language) speech in real time. The system supports translation into English, Chinese, and many other languages, and can display the subtitles in a floating overlay window.

Perfect for use in meeting documentation, language learning, or subtitle assistance scenarios.

---

## 🚀 How to Use

### 1. Preparation

Ensure the following files and folders are present:

- `RealTime_Jp2txt.exe`: The packaged executable program

- `API_Key.txt`: A plain text file containing your OpenAI API Key (GPT-4o compatible)

### 2. Configure API Key

- Create a plain text file named `API_Key.txt` with **a single line** containing your valid API Key, for example:
  
  ```
  sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
  ```

> ⚠️ **Do not upload or share `API_Key.txt` publicly.**

### 3. Launch the Program

- Double-click `RealTime_Jp2txt.exe` to start.

- A graphical interface will appear; no command line is required.

### 4. GUI Instructions

- **Keyword Input Box**: Optionally enter a keyword that describes the audio topic. This helps the model better understand the context.

- **Transcription Language Selection**: Choose the spoken language from the dropdown (default is Japanese). You can also select `auto` for automatic language detection.

- **Translation Language Selection**: Choose a target language for translating the transcribed text (default is English).

- **🎙️ Start Recording**: Begins real-time microphone recording. The system sends 4-second audio chunks to GPT-4o Transcribe for transcription.

- **⏹️ Stop Recording**: Immediately halts audio recording. Transcribed text remains visible.

- **🖥️ Floating Subtitles**: Opens a borderless, semi-transparent overlay window showing the two most recent lines of subtitles. It can be dragged, resized, and have its font adjusted.

- **Audio Level Bar**: Displays the current input volume level in real time.

- **Subtitle Display Area**: A scrollable area in the main window showing timestamped original and translated text in real time.

---

## 🧠 Features

### ✅ Real-Time Speech Recognition (with Contextual Overlap)

- Uses GPT-4o Transcribe API. Each audio chunk is 4 seconds with 0.8 seconds of overlap with the previous chunk to enhance contextual continuity.

### ✅ Keyword-Based Context Prompting

- The first transcription request includes the keyword entered by the user to help the model understand the context (e.g., "medical meeting", "news interview").

### ✅ Multi-Language Transcription & Translation

- **Transcription Supported Languages**:
  
  - Japanese (`ja`), English (`en`), Chinese (`zh`), Korean (`ko`), and more.
  
  - `auto` mode is supported for automatic language detection.

- **Translation Supported Languages**:
  
  - English, Japanese, Chinese, French, Spanish, Arabic, Indonesian, etc.

### ✅ Floating Subtitle Display

- A screen overlay window always stays on top, showing the latest two lines of subtitles.

- Ideal for displaying subtitles while running presentations (e.g., PowerPoint).

### ✅ Asynchronous Processing with Smooth GUI

- Multithreaded architecture ensures audio capture, transcription, and translation are processed independently.

- The main GUI thread remains responsive and fluid.

---

## 📂 File Structure

```
Translation/
├── RealTime_Jp2txt.exe             # Executable program (double-click to run)
├── API_Key.txt                     # Plain text file containing OpenAI API Key
├── Pycode/                         # Source code directory (Python modules)
│   └── RealTime_Transcription.py   # Main logic (if present)
```

| File/Folder Path      | Description                                 |
| --------------------- | ------------------------------------------- |
| `Translation/`        | Root directory containing all program files |
| `RealTime_Jp2txt.exe` | Main GUI executable, double-click to launch |
| `API_Key.txt`         | Contains your OpenAI API key                |
| `Pycode/`             | Source code folder for development purposes |
| `Pycode/*.py`         | Python source files                         |

> 🛠️ For developers: You may edit files in the `Pycode/` folder and repackage using PyInstaller.

---

## 💡 Notes

- Ensure a stable internet connection before launching to avoid API timeout errors.

- Your OpenAI account must have GPT-4o access to successfully call transcription and chat models.

---

## 📞 Support

If you encounter problems, please check the following first:

- Invalid API Key, insufficient permissions, or usage quota exhausted

- Network issues

- Microphone device not properly connected

- Audio format conversion failure (keep default settings)

---

Feel free to customize and build upon this system to create your own transcription solutions.

# 实时日语字幕转写系统（附带关键词功能）

## 🧩 简介

本程序是一款基于 GPT-4o API 的**多语种实时语音转写与翻译系统**，具有美观现代的图形界面。用户只需连接麦克风并点击“开始录音”，即可实时获取日语（或其他语言）语音的文字版本，支持翻译为英语、中文等多种语言，并通过浮动字幕窗口进行即时展示。

适用于会议记录、语言学习、字幕辅助等场景。

---

## 🚀 使用方法

### 1. 准备工作

- 确保文件夹中存在两个文件：
  
  - `RealTime_Jp2txt.exe`：已打包好的可执行程序
  
  - `API_Key.txt`：存放你自己的 OpenAI API Key（GPT-4o 版本支持）

### 2. 配置 API Key

- 创建一个名为 `API_Key.txt` 的纯文本文件，内容仅包含一行有效的 API Key，例如：
  
  ```
  sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
  ```

> ⚠️ **请勿将 API_Key.txt 上传至公开仓库或泄露给他人！**

### 3. 启动程序

- 双击 `RealTime_Jp2txt.exe` 启动程序。

- 程序启动后将出现图形界面，无需命令行操作。

### 4. 操作说明

- **关键词输入框**：填写当前语音主题关键词（可选），用于提高模型理解上下文的能力。

- **转写语言选择**：从下拉框中选择语音的语言（默认日语），也可以设置为 `auto` 自动检测。

- **翻译语言选择**：可以选择是否将识别结果翻译为其他语言，默认是英语。

- **🎙️ 开始录音**：点击后开始麦克风采集，系统将每 4 秒采样一次音频进行转写。

- **⏹️ 停止录音**：点击后立即停止采集音频，但已识别的文本不会丢失。

- **🖥️ 浮动字幕**：可打开一个无边框半透明窗口，用于在屏幕上实时展示最新两句字幕，可拖动/缩放/更改字体大小。

- **音频电平条**：实时展示当前音量强度。

- **字幕展示区**：主界面中间区域将实时滚动展示带时间戳的原文和翻译内容。

---

## 🧠 功能特点

### ✅ 实时语音识别（支持重叠上下文）

- 使用 GPT-4o Transcribe 接口，每段音频长度为 4 秒，且与上一段重叠 0.8 秒，以提升语义连贯性。

### ✅ 支持关键词语境提示

- 启动转写前填写的关键词会作为上下文注入首个请求，帮助模型理解语境（如“医学会议”、“新闻采访”等）。

### ✅ 支持多语言转写与翻译

- 转写语言支持：
  
  - `ja – 日本語`、`en – English`、`zh – 中文`、`ko – 한국어` 等十几种语言。
  
  - 支持 `auto` 自动语言识别。

- 翻译语言支持：
  
  - 英语、日语、中文、法语、西班牙语、阿拉伯语、印尼语等。

### ✅ 浮动字幕显示

- 支持屏幕底部弹出悬浮窗显示最近两句字幕，可缩放和调整字体大小，适合边开 PPT 边看字幕的场景。

### ✅ 异步处理与流畅界面

- 使用多线程机制确保音频采集、转写、翻译互不干扰。

- 主线程仅负责 GUI 更新，不卡顿、不崩溃。

---

## 📂 文件结构说明

Translation/
├── RealTime_Jp2txt.exe # 主程序，可执行文件（双击启动）
├── API_Key.txt # 存放 OpenAI API Key 的纯文本文件
├── Pycode/    # 源代码目录（Python 脚本与模块）  
│ └── RealTime_Transcription.py # 主程序逻辑（如有）

| 文件/文件夹路径              | 说明                       |
| --------------------- | ------------------------ |
| `Translation`         | 根目录，包含所有运行和源码文件          |
| `RealTime_Jp2txt.exe` | 打包好的 GUI 主程序，双击即可运行      |
| `API_Key.txt`         | 存放 OpenAI API Key 的纯文本文件 |
| `Pycode/`             | 源码文件夹，适用于开发者修改功能         |
| `Pycode/*.py`         | Python 脚本                |

---

## 💡 注意事项

- 每次启动前请确保网络连接稳定，否则可能出现 API 超时。

- OpenAI 账户需开通 GPT-4o 权限，确保你的 API Key 可正常调用音频和聊天模型。

---

## 📞 技术支持

如遇问题，请联系开发者，或确认是否为以下原因：

- API Key 错误，权限或余额不足

- 网络连接异常

- 麦克风设备未正确连接

- 音频格式转换失败（请保持默认配置）

---

如需制作自定义语言转写系统，欢迎在此基础上进行二次开发。
