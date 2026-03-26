# Shortcuts & Aliases I Don't Want to Forget

This document collects the main keyboard shortcuts and configurations I use in my development environment.

## 🖥️ Basic Setup

- **Operating System**: Ubuntu
- **Window Manager**: Pop Shell
- **Terminal Emulator**: Kitty
- **Shell**: Zsh with Oh-My-Zsh

## ⌨️ Kitty Terminal Shortcuts

### Window Management

| Action                   | Shortcut                |
|--------------------------|-------------------------|
| Open a new window (split)| `Ctrl + Shift + Enter`  |
| Next window              | `Ctrl + Shift + J`      |
| Previous window          | `Ctrl + Shift + K`      |

### Layout Management

| Action                   | Shortcut                |
|--------------------------|-------------------------|
| Next layout              | `Ctrl + Shift + L`      |
| Switch to Tall layout    | `Ctrl + Alt + R`        |
| Switch to Stack layout   | `Ctrl + Alt + S`        |

### Tab Management

| Action                   | Shortcut                |
|--------------------------|-------------------------|
| Open a new tab           | `Ctrl + Shift + T`      |
| Switch to next tab       | `Ctrl + Shift + →`      |
| Switch to previous tab   | `Ctrl + Shift + ←`      |
| Close current tab        | `Ctrl + Shift + Q`      |

### Font Size

| Action                   | Shortcut                |
|--------------------------|-------------------------|
| Reset font size          | `Ctrl + Shift + Backspace` |

## Tmux

| Action                   | Shortcut                |
|--------------------------|------------------------------------------|
| Start tmux               | `tmux`                                   |
| Create a named session   | `tmux new -s "session name"`             |
| Show tmux session        | `tmux ls`                                |
| Attach a session         | `tmux a -t "session name"`               |
| Close session            | `tmux kill-session -t "session name" `   |



## 🪟 Pop Shell Keyboard Shortcuts

| Action                                         | Shortcut                  |
|------------------------------------------------|---------------------------|
| Maximize window                                | `Super + M`               |
| Minimize window                                | `Super + ,`               |
| Toggle floating mode                           | `Super + Y`               |
| Minimize all window                            | `Super + D`               |
| Close window                                   | `Super + Q`               |
| Toggle notifications menu                      | `Super + V`               |
| Open a terminal                                | `Super + T`               |
| Open Files                                     | `Super + F`               |
| Move focus to the left window                  | `Super + Left Arrow`      |
| Move focus to the right window                 | `Super + Right Arrow`     |
| Move focus to the window above                 | `Super + Up Arrow`        |
| Move focus to the window below                 | `Super + Down Arrow`      |
| Enter window adjustment mode                   | `Super + enter`           |
| In window adjust mode change window dimension  | `shif + arrow key`        |

## 🐚 Shell Configuration

### Oh-My-Zsh Setup

**Theme:**
```bash
ZSH_THEME="af-magic"
```

**Plugins:**
```bash
plugins=(git docker docker-compose gcloud kubectl nvm zsh-autosuggestions zsh-syntax-highlighting)
```

### Environment Variables

| Variable        | Value           | Description                    |
|-----------------|-----------------|--------------------------------|
| `KUBE_EDITOR`   | `"code -w"`     | Default editor for kubectl    |

## 🔧 Useful Aliases

### General & System

| Alias              | Command                                              | Description                           |
|--------------------|------------------------------------------------------|---------------------------------------|
| `editzshrc`        | `code -w ~/.zshrc`                                  | Edit zsh configuration file           |
| `changeterminal`   | `sudo update-alternatives --config x-terminal-emulator` | Change default terminal emulator |

### Git

| Alias     | Command      | Description            |
|-----------|--------------|------------------------|
| `gis`     | `git status` | Quick git status check |

### Python Development

| Alias          | Command                        | Description                    |
|----------------|--------------------------------|--------------------------------|
| `createenv`    | `python3 -m venv .venv`        | Create Python virtual environment |
| `activateenv`  | `source .venv/bin/activate`    | Activate Python virtual environment |

### Docker

| Alias       | Command                              | Description                  |
|-------------|--------------------------------------|------------------------------|
| `dockclose` | `docker ps -a -q \| xargs -r docker stop` | Stop all Docker containers |

### Hardware & Custom Keyboard

| Alias          | Command                        | Description                                    |
|----------------|--------------------------------|------------------------------------------------|
| `enablewbhid`  | `sudo chmod 0666 /dev/hidraw*` | Enable WebHID for [custom keyboard](https://shop.yushakobo.jp/products/ergo68?srsltid=AfmBOooudKzfT2ei_vvEQ10X4z9P25RyCY7CwjRBGARdegu56czVlCKU) remapping |

> **Note**: The `enablewbhid` alias is needed before using [Remap](https://remap-keys.app/) to configure the custom keyboard layout.