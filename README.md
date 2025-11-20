# gitt - Interactive Git Add

An interactive command-line tool that makes staging files in Git easier and more visual.

## Features

- **Interactive checkbox interface** - Visual selection of files to stage
- **Keyboard navigation** - Arrow keys to navigate, Enter to select
- **Color-coded status** - Different colors for modified vs new files
- **Clean display** - See all unstaged changes at a glance
- **Simple workflow** - Select files, confirm, done

## Installation

### Manual Installation

1. Clone or download this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/gitt.git
   cd gitt
   ```

2. Make the script executable:
   ```bash
   chmod +x gitt
   ```

3. Move to a directory in your PATH:
   ```bash
   # Option 1: User bin directory
   mkdir -p ~/bin
   mv gitt ~/bin/
   echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc

   # Option 2: System-wide (requires sudo)
   sudo mv gitt /usr/local/bin/
   ```

### Homebrew (Coming Soon)

```bash
brew tap YOUR_USERNAME/gitt
brew install gitt
```

## Usage

Navigate to any Git repository and run:

```bash
gitt add
```

### Controls

- **↑/↓ Arrow Keys** - Navigate through files
- **Enter** - Select/deselect a file (toggle checkbox)
- **Enter on Confirm** - Stage all selected files

### Example

```
=== Interactive Git Add ===
Use ↑/↓ arrows to navigate, Enter to select/deselect

  [✓] M src/index.js
→ [ ] N src/utils.js
  [✓] M README.md

  [Confirm and stage selected files]
```

In this example:
- `M` = Modified file (shown in yellow)
- `N` = New untracked file (shown in green)
- `✓` = File is selected to be staged

## What Gets Shown

The tool displays:
- **Modified files** - Tracked files that have changes
- **New files** - Untracked files

The tool does NOT show:
- Staged files (already added)
- Deleted files

## Requirements

- Bash 3.2 or later (included with macOS and most Linux distributions)
- Git
- A terminal that supports ANSI color codes

## Why gitt?

The standard `git add` command requires you to type out file paths or use `git add -p` for interactive staging, which can be cumbersome. `gitt` provides a visual, checkbox-style interface that makes it easy to see all your changes and select exactly what you want to stage.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details

## Author

Created by Liron Katsif
# Gitt-Add-Tool
