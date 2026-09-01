# 🍅 Pomodoro Timer

A simple and elegant Pomodoro Timer application built with Python's **Tkinter** library. This app helps you manage your work sessions and breaks using the Pomodoro Technique.

## 📋 Overview

The Pomodoro Technique is a time management method that uses a timer to break work into focused intervals (typically 25 minutes) separated by short breaks.

### Features
- ⏱️ **Work Sessions**: 25-minute focused work periods
- 🎯 **Short Breaks**: 5-minute breaks between work sessions
- 🌟 **Long Breaks**: 20-minute breaks after every 4 work sessions
- ✅ **Progress Tracking**: Visual checkmarks show completed work sessions
- 🎨 **Colorful UI**: Clean interface with color-coded labels (green for work, pink for break, red for long break)
- 🎮 **Interactive Controls**: Start and Reset buttons for easy control

### Timer Cycle
1. Work - 25 minutes (GREEN)
2. Short Break - 5 minutes (PINK)
3. Work - 25 minutes (GREEN)
4. Short Break - 5 minutes (PINK)
5. Work - 25 minutes (GREEN)
6. Short Break - 5 minutes (PINK)
7. Work - 25 minutes (GREEN)
8. Long Break - 20 minutes (RED)
9. Cycle repeats...

## 🛠️ Requirements

- Python 3.6 or higher
- Tkinter (usually comes pre-installed with Python)
- Image file: `tomato.png` (must be in the same directory)

## 📦 Installation

### 1. Verify Python Installation
Open PowerShell/Terminal and run:
```bash
python --version
```

### 2. Install Tkinter (if not already installed)
**Windows:**
```bash
pip install tk
```

**macOS:**
```bash
brew install python-tk@3.11  # Replace 3.11 with your Python version
```

**Linux:**
```bash
sudo apt-get install python3-tk
```

### 3. Prepare the Tomato Image
The application requires a `tomato.png` image file in the same directory. 

**Option A: Add Your Own Image**
- Place any PNG image named `tomato.png` in the project directory

**Option B: Download Sample Image**
- Download a tomato icon from free resources like:
  - Pngimg.com
  - Flaticon.com
  - Pixabay.com
- Save it as `tomato.png` in the project directory

> Note: Ensure the image is at least 200x224 pixels for best display

## 🚀 How to Run

### Option 1: Run in VS Code (Recommended)
1. Open the project folder in VS Code
2. Click on the `main.py` file
3. Click the **"Run"** button (▶️) in the top-right corner
   - OR use keyboard shortcut: **Ctrl + F5**
   - OR use the terminal command below

### Option 2: Run from Terminal/PowerShell
```bash
python main.py
```

### Option 3: Set Up a VS Code Task (Advanced)
Create a `.vscode/tasks.json` file in your project root:
```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Run Pomodoro Timer",
      "type": "shell",
      "command": "python",
      "args": ["main.py"],
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "presentation": {
        "reveal": "always"
      }
    }
  ]
}
```

Then press **Ctrl + Shift + B** to run the task.

## 💡 Usage Instructions

1. **Start the Timer**: Click the **"Start"** button to begin a work session
2. **Follow the Timer**: Watch the countdown on the timer display
3. **Automatic Transitions**: The app automatically switches between work and break periods
4. **Track Progress**: Checkmarks (✅) appear at the bottom after each completed work session
5. **Reset Anytime**: Click the **"Reset"** button to clear the timer and start over

## 📄 Code Analysis

### Key Components

| Component | Purpose |
|-----------|---------|
| `start_timer()` | Initiates timer based on session type (work/break) |
| `count_down()` | Countdown mechanism that updates every second |
| `reset_timer()` | Clears timer and resets all values |
| `WORK_MIN`, `SHORT_BREAK_MIN`, `LONG_BREAK_MIN` | Configurable duration constants |
| `reps` | Counter to track total sessions for break type determination |

### Color Scheme
```python
PINK = "#e2979c"      # Short breaks
RED = "#e7305b"       # Long breaks
GREEN = "#9bdeac"     # Work sessions
YELLOW = "#f7f5dd"    # Background
```

### Customization Tips
To change timer durations, edit these constants at the top of `main.py`:
```python
WORK_MIN = 25        # Change to your preferred work duration
SHORT_BREAK_MIN = 5  # Change to your preferred short break
LONG_BREAK_MIN = 20  # Change to your preferred long break
```

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| "No module named 'tkinter'" | Install tk: `pip install tk` |
| "FileNotFoundError: tomato.png" | Ensure `tomato.png` is in the same directory as `main.py` |
| Timer window doesn't appear | Check if Python process is running; verify no console errors |
| Image not displaying | Verify the PNG file is valid and in the correct format |

## 📚 Project Structure
```
Pomodaro-Timer/
├── main.py           # Main application file
├── tomato.png        # Timer display image (required)
└── README.md         # This file
```

## 🎓 Learning Resources

- [Tkinter Documentation](https://docs.python.org/3/library/tkinter.html)
- [Pomodoro Technique](https://en.wikipedia.org/wiki/Pomodoro_Technique)
- [Python Timer Tutorial](https://www.pythontutorials.com/)

## 📝 License

Free to use and modify for personal or educational purposes.

## 🤝 Contributing

Feel free to enhance this project with features like:
- Sound notifications when timer ends
- Custom session durations via UI settings
- Data logging to track productivity
- Dark mode theme
- Session history and statistics

---

**Enjoy productive pomodoro sessions! 🍅⏱️**
