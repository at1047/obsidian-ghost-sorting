# obsidian-ghost-sorting

This plugin hides prefixes used for sorting in file and folder names in Obsidian while preserving the real filename to utilize native ordering behavior.

### Why this plugin
I wanted a way to sort files and folders that does not rely on metadata files and works in vanilla Obsidian as well as other text editors.

## Features

- **Automatic Detection**: Detects and hides sortable prefixes at the beginning of file/folder names
- **Flexible Patterns**: Supports underscore-number and omega-number prefixes:
  - `_1 Control Seminars` → `Control Seminars`
  - `_01 Notes` → `Notes`
  - `_1. Introduction` → `Introduction`
  - `_1- Chapter` → `Chapter`
- **Bottom Grouping with Omega**: Use `Ω_` + number to move notes to the bottom section while still sorting alphanumerically inside that section:
  - `Ω_1 Archive` → `Archive`
  - `Ω_20 Someday` → `Someday`
- **Hides in Multiple Places**: Numbers are hidden in:
  - File explorer sidebar
  - Page headings when files are opened
  - View headers

## How It Works

The plugin scans file and title UI elements and, when a supported sortable prefix is found, hides that prefix from display while keeping it in the real filename.

1. Detects a sortable prefix like `_1 ` or `Ω_1 `
2. Cleans the file name in the UI

## Supported Prefix Patterns

- `_1 ` (underscore + number + space)
- `_01 ` (underscore + zero-padded number + space)
- `_1. ` (underscore + number + dot + space)
- `_1- ` (underscore + number + dash + space)
- `Ω_1 ` (omega + underscore + number + space)
- `Ω_01 ` (omega + underscore + zero-padded number + space)

## Using Omega for Bottom Sorting

Use the uppercase omega character `Ω` as a high-sort prefix marker. Prefix notes with `Ω_` + number to keep them grouped at the bottom. You can obtain this symbol by copy and pasting it from the settings tab of this plugin.


## Installation

### Manual Installation

1. Download the plugin files (`main.js`, `manifest.json`, and `styles.css`)
2. Create a new folder in your vault: `.obsidian/plugins/obsidian-ghost-sorting/`
3. Copy all three files into this folder
4. Restart Obsidian or reload the app
5. Go to Settings → Community plugins
6. Enable "obsidian-ghost-sorting"

### Directory Structure

```
YourVault/
└── .obsidian/
    └── plugins/
        └── obsidian-ghost-sorting/
            ├── main.js
            ├── manifest.json
            └── styles.css
```

## Uninstalling

1. Disable the plugin in Settings → Community plugins
2. Delete the `.obsidian/plugins/obsidian-ghost-sorting/` folder
3. Restart Obsidian

The plugin will restore all original file name displays when disabled.

## License

MIT License - Feel free to modify and distribute as needed.

## Support

If you encounter any issues or have suggestions, please feel free to reach out!

