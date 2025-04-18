# ⚡ Rithwik's NixOS + Hyprland Setup

Welcome to my high-performance, battery-optimized, aesthetic-heavy Linux dev environment.  
This is a full-blown NixOS flake setup running Hyprland — built for clean visuals, raw speed, and full control over every package, pixel, and process.

## 💻 What’s Inside?

### 🧠 System

- **Distro:** NixOS (Flake-based)
- **WM:** Hyprland (Wayland compositor)
- **Shell:** Zsh + Fastfetch
- **Terminal:** Kitty + NerdFont
- **Editor:** AstroNvim (Neovim IDE)
- **Login:** greetd + Tuigreet

### 🎨 Aesthetic Stack

- **Theme:** Catppuccin Mocha + custom Waybar
- **Font:** JetBrainsMono Nerd Font
- **Blur + Shadows:** Hyprland shaders
- **Dynamic Wallpaper:** Hyprpaper

### 🧰 Dev Tools

- **AstroNvim** – LSP, Treesitter, Formatter, DAP
- **Zed Editor, Obsidian, VS Code** – via Flatpak
- **Git, Ripgrep, FD, Node, Python, Go** – installed via flake
- **Docker + Postman** – DevOps ready

### 📲 Connectivity

- **KDE Connect** (via Flatpak) for Android sync
- **Bluetooth + NetworkManager** available but optimized for power

---

## 🔋 Battery Optimization (Laptop-Tier Setup)

I’ve fully tuned this system for maximum battery life without compromising performance:

- **TLP** – Dynamic CPU, USB, PCIe, and WiFi power saving
- **zramSwap** – RAM compression for lower disk usage
- **CPU Governor:** Powersave mode when on battery
- **GPU:** Intel PSR enabled
- **Charging Thresholds:** 40–80% via Lenovo conservation mode
- **powertop --auto-tune** ready for on-demand optimization

---

## 📀 Flake Structure

```bash
NixOS-Hyprland/
├── flake.nix
├── flake.lock
├── hosts/
│   └── rithwik/
│       ├── config.nix
│       ├── packages-fonts.nix
│       ├── users.nix
│       └── variables.nix
└── modules/
    └── intel-drivers.nix (plus others)
```

This structure is built for scalability, modularity, and clean rebuilds.

---

## 🔧 System Commands

| Task                     | Command                                       |
| ------------------------ | --------------------------------------------- |
| Rebuild system           | `sudo nixos-rebuild switch --flake .#rithwik` |
| Clean old builds         | `sudo nix-collect-garbage -d`                 |
| Optimize power live      | `sudo powertop --auto-tune`                   |
| Check battery health     | `sudo tlp-stat -b`                            |
| Pair phone (KDE Connect) | `flatpak run org.kde.kdeconnect`              |

---

## 🚀 Why NixOS?

Because I want full control.  
I can:

- Reproducibly rebuild my entire dev machine in minutes
- Track every dependency
- Optimize battery, visuals, and performance declaratively
- Never touch a broken apt/pacman system again

---

## ⚔️ Setup Philosophy

> “Make it beautiful. Make it fast. Make it yours.”

No bloat, no fluff.  
Just a clean Linux war machine, optimized for battery life, coding, and aesthetic flow.

---

## 📸 Screenshots

> _Drop your sexy rice screenshots here once you’re done flexing._

---

## 📩 TODO / Next Additions

- [ ] Auto low-battery notifications
- [ ] LazyGit + Neogit integration
- [ ] Custom AstroNvim statusline
- [ ] Auto-brightness based on battery level

---

## 🧙‍♂️ Inspired By

- [JaKooLit](https://github.com/JaKooLit)
- [AstroNvim](https://github.com/AstroNvim)
- [Catppuccin](https://github.com/catppuccin)

---

## 🧠 Pro Tip

> “Never settle for defaults. If it doesn’t feel like yours — rebuild it.”
