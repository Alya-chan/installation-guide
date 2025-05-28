# Visual Studio Code Local Development Setup Guide

![VS Code](https://code.visualstudio.com/assets/images/code-stable.png)

**Set up Visual Studio Code (VS Code) as your ultimate local development environment.**  
This guide covers everything from installation to advanced tips, including Git & GitHub integration, debugging, and platform-specific instructions for Windows, macOS, and Linux.

---

## 🚀 Ultimate Visual Studio Code Setup for Local Development

Whether you're a beginner or a seasoned developer, this guide empowers you to harness the full potential of VS Code. You'll learn how to supercharge your productivity, master version control, streamline debugging, and customize your environment across all major platforms.

---

## 🤔 Why VS Code?

Why do millions choose VS Code as their editor of choice?

- **Lightweight & Fast** — Launches instantly and stays snappy even on large projects.
- **Extensible Marketplace** — Thousands of extensions tailor your setup for any language or workflow.
- **Built-in Power Features** — IntelliSense, debugging, integrated terminal, and Git, all ready out-of-the-box.
- **Cross-Platform Consistency** — Same great experience on Windows, macOS, and Linux.
- **Vibrant Community & Updates** — Regular improvements backed by Microsoft and an active developer base.

---

## 📋 Table of Contents

1. [Install VS Code](#1-install-vs-code)  
2. [Configure Basic Settings](#2-configure-basic-settings)  
3. [Essential Extensions](#3-essential-extensions)  
4. [Master Git & GitHub Integration](#4-master-git--github-integration)  
5. [Become a Debugging Pro](#5-become-a-debugging-pro)  
6. [Linux Power-User Setup](#6-linux-power-user-setup)  
7. [Pro Tips & Tricks](#7-pro-tips--tricks)  
8. [Troubleshooting](#8-troubleshooting)  
9. [Further Reading](#9-further-reading)  

---

## 1. 🛠️ Install VS Code

Start by downloading the latest VS Code installer from the official site:  
➡️ [Download Visual Studio Code](https://code.visualstudio.com/Download)

- **Windows & macOS:** Run the installer and follow prompts.  
- **Linux:** See [Section 6](#6-linux-power-user-setup) for detailed instructions.

---

## 2. ⚙️ Configure Basic Settings

Personalize VS Code to match your workflow.

- Open Settings:  
  - Windows/Linux: *File > Preferences > Settings*  
  - macOS: *Code > Preferences > Settings*  
  - Shortcut: `Ctrl + ,` (Win/Linux) or `Cmd + ,` (macOS)

### Recommended Settings

| Setting                            | Description                                    | Example / Notes                                    |
|----------------------------------|------------------------------------------------|--------------------------------------------------|
| **Theme**                        | Choose a color theme                           | Search Extensions: *One Dark Pro, Monokai Pro*   |
| **Font Family**                  | Set coding font                                | `'Fira Code', Consolas, Menlo, monospace`        |
| **Font Size**                    | Adjust font size                              | `14` (adjust to your preference)                  |
| **Minimap**                     | Enable code overview map                       | `editor.minimap.enabled: true`                    |
| **Line Numbers**                | Show line numbers (default: on)                | Options: `on`, `relative`, `off`                  |
| **Bracket Pair Colorization**   | Visual aid for matching brackets                | `editor.bracketPairColorization.enabled: true`   |
| **Tab Size & Indentation**      | Consistency in tabs/spaces                      | `editor.tabSize: 2 or 4` + `editor.insertSpaces: true` |
| **Word Wrap**                   | Control line wrapping                           | `editor.wordWrap: on` for Markdown, off for code  |
| **Format on Save**              | Auto-format your code on save                   | `editor.formatOnSave: true` (needs formatter extension) |
| **Auto Save**                   | Save files automatically                        | `files.autoSave: afterDelay`, `files.autoSaveDelay: 1000` ms |

---

## 3. 🧩 Essential Extensions

Boost your workflow by installing these highly recommended extensions via the Extensions sidebar (`Ctrl+Shift+X` or `Cmd+Shift+X`):

| Extension             | Why You Need It                             | Publisher      |
|-----------------------|--------------------------------------------|----------------|
| **GitLens**           | Supercharge Git history & code insights    | GitKraken      |
| **Prettier**          | Opinionated code formatter                   | Prettier       |
| **Live Server**        | Local web server with live reload            | Ritwick Dey    |
| **ESLint**            | JavaScript/TypeScript linting                | Microsoft      |
| **Path Intellisense** | Autocomplete file paths                       | Christian Kohler |
| **Material Icon Theme** | Beautiful icons for files/folders           | Philipp Kief   |
| **TODO Highlight**    | Visually track TODOs & FIXMEs                 | Wayou Liu      |
| **Remote - SSH**      | Develop on remote machines                    | Microsoft      |
| **Docker**            | Manage containers & images                     | Microsoft      |
| **Debugger for [Language]** | Language-specific debugging tools         | Microsoft      |

> **Pro Tip:** For language-specific needs, search for official or top community extensions (e.g., *Pylance* for Python, *Volar* for Vue).

---

## 4. 🐙 Master Git & GitHub Integration

VS Code makes Git seamless, here’s how to get started:

### Install Git

- **Windows:** [Download Git for Windows](https://git-scm.com/download/win)  
  - Choose *Git from the command line and also from 3rd-party software* during setup.  
- **macOS:** Comes with Xcode Command Line Tools or install via Homebrew:  
  ```bash
  brew install git
  ```  
- **Linux:** Use your distro’s package manager (see Section 6.2).

### Configure Git Identity

Open VS Code terminal (`Ctrl + \`` / `Cmd + \``):  
```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.email@example.com"
```

### Use Git Inside VS Code

- **Source Control Panel** (`Ctrl+Shift+G` / `Cmd+Shift+G`): stage, commit, branch, push, pull, and more.  
- **Integrated Terminal:** run any Git commands directly.  
- **Command Palette:** type `Git:` to access Git commands quickly.

### Connect to GitHub

- **Authentication:** VS Code prompts GitHub sign-in on first push/pull of private repos.  
- **Use SSH keys or Personal Access Tokens (PATs)** for secure access.  
- **Clone repos:** via Command Palette `Git: Clone` or terminal `git clone <url>`.  
- **Publish local project:**  
  ```bash
  git init -b main
  git add .
  git commit -m "Initial commit"
  git remote add origin <github_repo_url>
  git push -u origin main
  ```
- VS Code also supports **Publish to GitHub** button for quick repo creation.

---

## 5. 🐞 Become a Debugging Pro

Debug your code directly in VS Code with powerful tools:

- Set breakpoints by clicking left margin or pressing `F9`.  
- Use the **Run and Debug** view (`Ctrl+Shift+D` / `Cmd+Shift+D`).  
- Configure launch settings in `.vscode/launch.json` for complex scenarios.  
- Debug Node.js, Python, C++, Java, and more with official debugger extensions.

---

## 6. 🐧 Linux Power-User Setup

### Install VS Code on Linux

#### Ubuntu/Debian

```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

#### Fedora

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]
name=Visual Studio Code
baseurl=https://packages.microsoft.com/yumrepos/vscode
enabled=1
gpgcheck=1
gpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
sudo dnf check-update
sudo dnf install code
```

### Install Git on Linux

Ubuntu/Debian:

```bash
sudo apt install git
```

Fedora:

```bash
sudo dnf install git
```

---

## 7. 🎯 Pro Tips & Tricks

- **Settings Sync:** Use built-in Settings Sync (`Settings > Turn on Settings Sync`) to keep settings/extensions across devices.  
- **Keyboard Shortcuts:** Customize (`File > Preferences > Keyboard Shortcuts`) to speed up workflow.  
- **Multi-root Workspaces:** Work on multiple projects simultaneously.  
- **Snippets:** Create custom code snippets for repetitive code.  
- **Integrated Terminal:** Use split terminals, customize shells, and shortcuts.  
- **Remote Development:** Use Remote Containers, SSH, and WSL extensions for remote workflows.  
- **Workspaces:** Save different folder setups as workspace files for quick project switching.

---

## 8. 🛠️ Troubleshooting

- **Extension Issues:** Disable all extensions and enable one by one to find culprit.  
- **Performance:** Disable minimap, reduce animation, close unused editors.  
- **Git Issues:** Check Git path in settings, update Git to latest version.  
- **Debugging Fails:** Verify `launch.json` config and dependencies.  
- **Community Help:** Visit [VS Code GitHub](https://github.com/microsoft/vscode) or Stack Overflow.

---

## 9. 📚 Further Reading & Resources

- [VS Code Official Documentation](https://code.visualstudio.com/docs)  
- [Git Documentation](https://git-scm.com/doc)  
- [GitHub Docs](https://docs.github.com/en)  
- [Awesome VS Code Extensions List](https://github.com/viatsko/awesome-vscode)  
- [VS Code YouTube Tutorials](https://www.youtube.com/channel/UC8n8ftV94ZU_DJLOLtrpORA)

---

*Happy coding with Visual Studio Code! 🚀*

---

*This guide is continuously updated with best practices and latest features. Feel free to contribute or suggest improvements.*
