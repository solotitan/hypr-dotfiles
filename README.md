# 🌊 Hyprland Dotfiles

```
BE AWARE THAT I DO NOT UPDATE THIS REPO AS CHANGES ARE ROLLED OUT FOR HYPRLAND
SOME FILES LIKE hyprland.conf AND windowrules.conf MAY HAVE UPDATED OR DEPRECIATED SPECS
THESE ARE JUST BASE FILES I USE AS A START WHEN CONFIGURING MY HYPRLAND SETUPS
ODDS ARE IT WONT WORK OUT OF THE BOX AND WILL NEED SOME TWEAKING
```

A comprehensive and well-organized Hyprland configuration featuring modular configs, custom scripts, and beautiful theming. This setup provides a powerful and efficient Wayland desktop environment.

## ✨ Features

- **Modular Configuration**: Well-organized config files for easy maintenance
- **Custom Scripts**: Utility scripts for enhanced functionality
- **Beautiful Theming**: Consistent visual design across the desktop
- **Performance Optimized**: Smooth animations and efficient resource usage
- **NVIDIA Support**: Proper configuration for NVIDIA graphics cards
- **Comprehensive Keybindings**: Intuitive and efficient keyboard shortcuts
- **Window Management**: Advanced window rules and workspace management

## 📁 Structure

```
hypr/
├── Main Configuration Files:
│   ├── hyprland.conf          # Main Hyprland configuration
│   ├── keybindings.conf       # Custom keybindings
│   ├── windowrules.conf       # Window rules and management
│   ├── monitors.conf          # Monitor configuration
│   ├── animations.conf        # Animation settings
│   ├── hypridle.conf          # Idle management
│   ├── hyprlock.conf          # Lock screen configuration
│   ├── nvidia.conf            # NVIDIA-specific settings
│   ├── userprefs.conf         # User preferences
│   └── pyprland.toml          # Pyprland configuration
├── configs/                   # Modular configuration files
│   ├── binds.conf             # Additional keybindings
│   ├── env.conf               # Environment variables
│   ├── input.conf             # Input device settings
│   ├── misc.conf              # Miscellaneous settings
│   ├── monitors.conf          # Monitor setup
│   ├── plugins.conf           # Plugin configurations
│   └── workspaces.conf        # Workspace management
├── scripts/                   # Utility scripts
│   ├── autostart/             # Startup scripts
│   ├── hyprshot               # Screenshot utility
│   ├── hyprfreeze             # Window freezing utility
│   ├── color_picker           # Color picker tool
│   ├── random_wallpaper       # Wallpaper changer
│   ├── toggle_floating        # Toggle floating windows
│   ├── performance            # Performance management
│   └── portal                 # Portal configuration
├── themes/                    # Theme configurations
│   ├── theme.conf             # Main theme settings
│   ├── colors.conf            # Color definitions
│   └── common.conf            # Common theme elements
└── plugins/                   # Plugin configurations
```

## 🛠️ Requirements

### Essential Dependencies
- **Hyprland** (latest version recommended)
- **HyprPanal** (status bar)
- **Wofi** or **Rofi** (application launcher)
- **Kitty** or **Alacritty** (terminal emulator)
- **Swww** (wallpaper daemon)
- **Grim** + **Slurp** (screenshot tools)
- **Wl-clipboard** (clipboard utilities)

### Optional Dependencies
- **Hypridle** (idle management)
- **Hyprlock** (lock screen)
- **Pyprland** (additional functionality)
- **Dunst** or **Mako** (notifications)
- **Thunar** or **Nautilus** (file manager)

### For NVIDIA Users
- **NVIDIA drivers** (proprietary)
- **nvidia-vaapi-driver**
- **libva-nvidia-driver**

## 📦 Installation

### Quick Setup

1. **Backup your existing configuration**:
   ```bash
   mv ~/.config/hypr ~/.config/hypr.backup
   ```

2. **Clone this repository**:
   ```bash
   git clone https://github.com/solotitan/hypr-dotfiles.git ~/.config/hypr
   ```

3. **Make scripts executable**:
   ```bash
   chmod +x ~/.config/hypr/scripts/*
   ```

4. **Install dependencies** (Arch Linux example):
   ```bash
   paru -S hyprland waybar wofi kitty swww grim slurp wl-clipboard hypridle hyprlock
   ```

5. **Start Hyprland**:
   ```bash
   Hyprland
   ```

### Manual Installation

1. Create the hypr config directory:
   ```bash
   mkdir -p ~/.config/hypr
   ```

2. Copy all files from this repository to `~/.config/hypr/`

3. Adjust configurations according to your system (monitors, input devices, etc.)

## ⌨️ Key Bindings

### Essential Shortcuts
- `SUPER + Return` - Open terminal
- `SUPER + D` - Application launcher
- `SUPER + Q` - Close window
- `SUPER + M` - Exit Hyprland
- `SUPER + V` - Toggle floating
- `SUPER + F` - Toggle fullscreen
- `SUPER + L` - Lock screen

### Window Management
- `SUPER + Arrow Keys` - Move focus
- `SUPER + SHIFT + Arrow Keys` - Move windows
- `SUPER + 1-9` - Switch workspaces
- `SUPER + SHIFT + 1-9` - Move window to workspace

### Screenshots
- `Print` - Screenshot area
- `SUPER + Print` - Screenshot window
- `SHIFT + Print` - Screenshot full screen

> **Note**: Full keybinding list available in `keybindings.conf`

## 🎨 Customization

### Monitors
Edit `monitors.conf` to match your display setup:
```conf
monitor=DP-1,1920x1080@144,0x0,1
monitor=HDMI-A-1,1920x1080@60,1920x0,1
```

### Themes
Modify theme files in the `themes/` directory:
- `theme.conf` - Main theme settings
- `colors.conf` - Color scheme
- `common.conf` - Shared theme elements

### Scripts
All scripts in the `scripts/` directory are customizable:
- Edit script parameters to match your preferences
- Add new scripts for additional functionality

### Keybindings
Customize keybindings in:
- `keybindings.conf` - Main keybindings
- `configs/binds.conf` - Additional bindings

## 🚀 Scripts Overview

### Screenshot Tools
- **hyprshot**: Advanced screenshot utility with area/window/fullscreen modes
- **color_picker**: Pick colors from anywhere on screen

### Window Management
- **hyprfreeze**: Freeze/unfreeze windows for performance
- **toggle_floating**: Toggle window floating state
- **move_by_rules**: Apply window rules dynamically

### System Utilities
- **performance**: Switch between performance profiles
- **random_wallpaper**: Cycle through wallpapers
- **portal**: Configure XDG desktop portal

## 🔧 Troubleshooting

### Common Issues

**Hyprland won't start:**
- Check if all dependencies are installed
- Verify NVIDIA configuration (if applicable)
- Check logs: `journalctl -u display-manager`

**Performance issues:**
- Run the performance script: `~/.config/hypr/scripts/performance`
- Disable animations temporarily in `animations.conf`
- Check NVIDIA settings in `nvidia.conf`

**Scripts not working:**
- Ensure scripts are executable: `chmod +x ~/.config/hypr/scripts/*`
- Check script dependencies
- Verify paths in script files

### NVIDIA Specific
If using NVIDIA graphics:
1. Ensure `nvidia.conf` is properly configured
2. Check environment variables in `configs/env.conf`
3. Verify NVIDIA drivers are properly installed

## 🤝 Contributing

Feel free to submit issues and pull requests! Contributions are welcome for:
- Bug fixes
- Performance improvements
- New scripts and utilities
- Documentation improvements

## 📄 License

This configuration is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [Hyprland](https://hyprland.org/) - Amazing Wayland compositor
- [Hyprland Community](https://github.com/hyprwm/Hyprland) - For continuous development
- Various script authors and contributors

---

**Enjoy your beautiful Hyprland setup! 🌊✨**
