# 🧠 UiPath – Keyboard Automation (Simulate Keystrokes in Notepad)

This repository contains a **UiPath automation workflow** that demonstrates how to:
- **Open Notepad automatically**
- **Simulate keyboard typing (keystrokes)**
- **Use keyboard shortcuts (Ctrl + S, Alt + F4)**
- **Save and close a file** using UI Automation

---

## 📘 Project Overview
- Built using **UiPath Studio (Modern Design Experience)**
- Demonstrates use of **Start Process**, **Attach Window**, **Type Into**, and **Send Hotkey** activities
- Designed for **beginners** to understand basic **desktop keyboard automation**

---

## 📂 Project Files
| File | Description |
|------|--------------|
| `Main.xaml` | Main UiPath workflow (core logic) |
| `project.json` | UiPath project configuration file |
| `.gitignore` | (Optional) Ignore unnecessary UiPath folders when pushing to GitHub |

---

## 🧩 Workflow Logic

### 🔹 Step 1 – Start Notepad
- Uses the **Start Process** activity to launch Notepad (`notepad.exe`)

### 🔹 Step 2 – Type Text
- Uses **Type Into** activity with `Simulate Type` mode enabled  
- Automatically types: Yoo here bala - this is automated typing from UiPath!
- - `ClickBeforeTyping` ensures Notepad is focused before typing

### 🔹 Step 3 – Save File (Ctrl + S)
- Uses **Send Hotkey** activity with:
- Key: `s`
- Modifier: `Ctrl`
- Triggers the **Save As** dialog box

### 🔹 Step 4 – Enter Filename
- In the Save As dialog:
- **Type Into** the filename field:  
  `C:\Users\Public\Desktop\UiPath_AutoFile.txt`
- **Send Hotkey** → `Enter` to confirm and save

### 🔹 Step 5 – Close Notepad
- Uses **Send Hotkey** activity:
- Key: `w`
- Modifier: `Alt`
- This closes Notepad automatically

---

## 🧠 Example Run (Steps Overview)

| Step | Action | Description |
|------|---------|--------------|
| 1 | Launch Notepad | UiPath opens Notepad automatically |
| 2 | Type text | Simulates keystrokes to write content |
| 3 | Ctrl + S | Opens the Save As dialog |
| 4 | Type file name | Enters file name and saves file |
| 5 | Alt + F4 | Closes Notepad |

---

## ⚙️ Activities Used
| Activity | Purpose |
|-----------|----------|
| **Start Process** | Launches the Notepad application |
| **Attach Window** | Focuses on the Notepad or Save As window |
| **Type Into** | Types text or filename |
| **Send Hotkey** | Simulates keyboard shortcuts (Ctrl+S, Alt+F4) |
| **Delay** | Adds wait time for UI stability |

---


---

## 🧰 Requirements
- **UiPath Studio** (Community or Enterprise Edition)
- **UiPath.UIAutomation.Activities** package
- Windows 10 or 11

---

## 💡 Tips
- If keystrokes don’t register, try changing `Input Mode` in **Type Into** from `SimulateType` → `SendWindowMessages`
- Ensure UiPath and Notepad run under the same permission level (both as normal user or both as admin)
- Add small **Delay** activities (1–2 seconds) between steps for smoother execution

---

## 🖥️ Example Output
When you run the workflow:
1. Notepad opens automatically  
2. The text is typed line by line  
3. File is saved on your **Desktop** as `UiPath_AutoFile.txt`  
4. Notepad closes automatically  

---

## 📸 Screenshots
*(You can add your own screenshots like these)*

| Step | Screenshot |
|------|-------------|
| Open Notepad | ![Open Notepad](https://github.com/user-attachments/assets/example1.png) |
| Type Text | ![Type Text](https://github.com/user-attachments/assets/example2.png) |
| Save As Dialog | ![Save File](https://github.com/user-attachments/assets/example3.png) |

---

## 🧑‍💻 Author
**Bala Saravanan K**  
> Exploring automation with UiPath and RPA concepts ✨  

---

## 🏁 License
This project is open-source and available under the **MIT License**.

---


