# NvimQt macOS App Bundle

Create a simple `.app` bundle to launch `nvim-qt` GUI on macOS easily from Spotlight.

---

## Why?

Neovim Qt (`nvim-qt`) doesn’t come with a native macOS `.app` bundle by default. This repo provides an easy way to create one so you can launch it like any other macOS app.

---

## Features

- Simple `.app` bundle launcher for `nvim-qt`
- Custom app icon included
- Easy to build with a single script
- Works on macOS without needing Xcode

---

## Installation

### Prerequisites

- `nvim-qt` installed and accessible via `/usr/local/bin/nvim-qt` (adjust script if different)
- macOS system with Terminal access

### Build the app:

```bash
git clone https://github.com/jpadamsonline/nvim-qt-macos-app.git
cd nvim-qt-macos-app/scripts
chmod +x create_app.sh
./create_app.sh
```

This creates NvimQt.app in the repo root.

### Move the app to your Applications folder:

```bash
mv ../NvimQt.app ~/Applications/
```

Now you can launch NvimQt from Spotlight.


## Customization

If your nvim-qt executable is in a different path, edit the launcher script in scripts/create_app.sh accordingly.

To update the app icon, replace the file in resources/icon.icns and rebuild.


## Troubleshooting

If Spotlight doesn’t show the app, try:

mdimport ~/Applications/NvimQt.app

or restart your Mac.


## License

MIT


## Contributions

Feel free to open issues or pull requests! Your feedback and improvements are welcome.


## Credits

Created by @jpadamsonline


