# NeoMacVim

A lightweight macOS app bundle wrapper to launch the official [nvim-qt](https://github.com/neovim/neovim-qt) GUI client for Neovim.

---

## What is NeoMacVim?

NeoMacVim is **not** another Neovim GUI. Instead, it provides a simple native macOS `.app` wrapper that lets you launch the existing `nvim-qt` binary from Spotlight, Alfred, Raycast, Finder, or the Dock—just like any regular macOS app.

This solves the issue that `nvim-qt` doesn’t come with a native `.app` bundle by default on macOS.

---

## Why?

The official Neovim Qt client (`nvim-qt`) lacks a native macOS `.app` bundle. This project offers an easy way to create one, allowing you to launch `nvim-qt` like any other app on macOS.

---

## Features

- Simple `.app` bundle launcher for `nvim-qt`
- Custom app icon included
- Easy to build with a single script
- Works on macOS without Xcode
- No need to compile or package `nvim-qt` itself
- Launch from Spotlight, Dock, or Finder like any other macOS app

---

## Installation

### Prerequisites

- `nvim-qt` installed and accessible via `/usr/local/bin/nvim-qt` (adjust script if different)
- macOS system with Terminal access

### Build the app:

```bash
git clone https://github.com/jpadamsonline/neo-mac-vim.git
cd neo-mac-vim/scripts
chmod +x create_app.sh
./create_app.sh
```

This creates NeoMacVim.app in the repo root.

### Move the app to your Applications folder:

```bash
mv ../NeoMacVim.app ~/Applications/
```

Now you can launch NeoMacVim from Spotlight, Alfred, or Raycast.


## Customization

If your nvim-qt executable is in a different path, edit the launcher script in scripts/create_app.sh accordingly.

To update the app icon, replace the file in resources/icon.icns and rebuild.


## Troubleshooting

If Spotlight doesn’t show the app, try:

mdimport ~/Applications/NeoMacVim.app

or restart your Mac.


## License

MIT


## Contributions

Feel free to open issues or pull requests! Your feedback and improvements are welcome.


## Credits

Created by @jpadamsonline


