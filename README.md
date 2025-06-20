# DevCursor
# 🖱️ CodeCursor – AI-Powered Terminal Agent

**CodeCursor** is a terminal-based intelligent agent that operates like a smart cursor. It plans, acts, observes, and responds using structured reasoning cycles. It can generate code files, execute commands, edit content, and even check the weather – all through simple natural language instructions.

---

## 🎥 Demo Video

<p align="center">
  <a href="https://www.youtube.com/watch?v=W-acj5qVz8I">
    <img src="https://img.youtube.com/vi/W-acj5qVz8I/0.jpg" alt="Watch the demo" width="600">
  </a>
</p>




---

## ✨ Features

- 🔁 **Reasoning Loop**: Plan → Act → Observe → Respond
- 🧠 Intelligent code generation and file editing
- 📂 Automatically writes and organizes project files
- 📡 Get real-time weather for any city
- 🖥️ Execute valid Windows terminal commands
- 💾 Stores generated code in memory before writing
- 💬 Fully JSON-driven response protocol

---

## 🛠️ Built With

- Python 3.10+
- OpenAI (or Gemini-compatible) API
- dotenv for environment variables
- Requests, subprocess, os modules

---

## 📦 Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/codecursor.git
   cd codecursor
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure API Key**
   Create a `.env` file:
   ```
   GEMINI_API_KEY=your_gemini_or_openai_compatible_key
   ```

4. **Run the Agent**
   ```bash
   python main.py
   ```

---

## 🧑‍💻 Usage

Once running, just type your command into the terminal. Examples:

```bash
> Create a calculator app with HTML, CSS, and JavaScript
```

The agent will:
- Plan the steps
- Generate file content
- Store each file in memory
- Write them to disk via `write_file`

---

## 🛠️ Available Tools

| Tool Name     | Description                                | Input Type         |
|---------------|--------------------------------------------|--------------------|
| `get_weather` | Returns weather for a given city           | `string` (city name) |
| `run_command` | Executes Windows command-line instructions | `string` (cmd.exe command) |
| `write_file`  | Writes stored file content to disk         | `{ filepath, content }` |

---

## 🔒 Safety & Constraints

- Only valid `cmd.exe` commands are supported
- All agent responses must follow strict JSON format
- Final step must output a completion message before stopping

---

## 📂 Example Output

```json
{
  "step": "output",
  "content": "Project 'Calculator' created successfully. Files: index.html, styles.css, script.js are located in the 'Calculator' directory."
}
```
