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
