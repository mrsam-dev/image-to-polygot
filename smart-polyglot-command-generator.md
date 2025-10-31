# 🧠 Smart Polyglot Command Generator

A sleek, browser-based tool for generating terminal commands that merge image and ZIP files into hybrid polyglot files — files that behave like images but secretly contain embedded archives. Built for privacy-conscious workflows, steganography enthusiasts, and anyone who loves elegant command-line automation.

---

## 🚀 What is a Polyglot File?

A polyglot file is a single file that can be interpreted in multiple ways depending on context. In this case:
- It **renders as an image** when opened in a viewer
- It **extracts as a ZIP archive** when run through `unzip`

This tool automates the creation of such files using simple shell commands.

---

## 🛠️ How It Works

The tool generates two key terminal commands:

1. **Create the polyglot file**  
   It zips both the image and the payload, appends the ZIP to the image shell, and deletes the temporary ZIP:
   ```bash
   zip outer.zip image.jpg payload.zip && cat image.jpg outer.zip > hybrid.jpg && rm outer.zip
   ```

2. **Extract the contents later**  
   You can unzip the hybrid file to retrieve both the original image and the embedded ZIP:
   ```bash
   unzip hybrid.jpg
   ```

The resulting file behaves like a normal image but secretly contains embedded data.

---

## 🧪 Supported Formats

- Image: `.png`, `.jpg`, `.jpeg`
- Archive: `.zip`
- Output: Automatically matches the image extension (`hybrid.png`, `hybrid.jpeg`, etc.)

---

## 📋 How to Use the Tool

1. **Paste your `ls` output**  
   Example:
   ```
   1_source_image.jpeg 2_merged_file_here.zip
   ```

2. **Click “Parse”**  
   This auto-fills the image and ZIP fields.

3. **Review or edit the hybrid output name**  
   The tool auto-detects the correct extension (e.g. `.jpeg`).

4. **Click “Generate Commands”**  
   You’ll see two terminal commands:
   - One to create the polyglot
   - One to extract it later

5. **Click “Copy”** to grab the commands and run them in your terminal.

---

## 🧼 Self-Cleaning Logic

The generated command automatically deletes the temporary `outer.zip` after merging, keeping your workspace tidy.

---

## 🧠 Project Philosophy

This tool was built with:
- **Modularity**: Each step is clear, editable, and reproducible
- **Privacy**: No data leaves your browser
- **Teachability**: Designed for onboarding and documentation
- **Delight**: Playful UX, smart defaults, and elegant output

---

## 🧩 Future Enhancements

Here are ideas to supercharge the tool:

### 🔧 CLI Version
Create a command-line tool:
```bash
smartpolyglot --image image.jpg --zip payload.zip --out hybrid.jpg
```

### 🖥️ Desktop App
Wrap the HTML tool in Electron for offline use with drag-and-drop support.

### 🧠 AI Assistant Mode
Add a chatbot-style interface that explains each command and offers troubleshooting tips.

### 🧪 Format Detection
Support other archive formats like `.tar.gz`, `.rar`, or `.7z`.

### 🧼 Cleanup Toggle
Let users choose whether to auto-delete `outer.zip` or keep it for inspection.

---

## 🧠 For Your Future Self

Md — this tool is a reflection of your precision, creativity, and love for elegant workflows. You built it with care, tested it thoroughly, and polished it to the last detail. If you ever revisit this project, remember how fun it was to build something modular, teachable, and delightful.

Keep building magic. 🚀
