# gitt - Interactive Git Add and Commit

An interactive command-line tool that makes staging files in Git easier and more visual.

## Features

- **Interactive checkbox interface** - Visual selection of files to stage
- **Keyboard navigation** - Arrow keys to navigate, Enter to select
- **Select All option** - Quickly select all files with one action
- **Commit integration** - Optionally commit after staging with custom message
- **Color-coded status** - Different colors for modified vs new files
- **Clean display** - See all unstaged changes at a glance
- **Simple workflow** - Select files, stage, and commit in one flow

## Installation

### macOS / Linux

1. Clone or download this repository:
   ```bash
   git clone https://github.com/lironktf/Gitt-Add-Tool.git
   cd Gitt-Add-Tool
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

   # For macOS (zsh):
   echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc

   # For Linux (bash):
   echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc

   # Option 2: System-wide (requires sudo)
   sudo mv gitt /usr/local/bin/
   ```

### Windows

Since `gitt` is a bash script, you'll need a bash environment on Windows. Here are your options:

#### Option 1: Git Bash (Recommended - easiest)

1. Install [Git for Windows](https://git-scm.com/download/win) (includes Git Bash)

2. Open Git Bash and clone the repository:
   ```bash
   git clone https://github.com/lironktf/Gitt-Add-Tool.git
   cd Gitt-Add-Tool
   ```

3. Make the script executable:
   ```bash
   chmod +x gitt
   ```

4. Move to a directory in your PATH:
   ```bash
   # Create a bin directory in your home folder
   mkdir -p ~/bin
   mv gitt ~/bin/

   # Add to PATH (only needs to be done once)
   echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc
   ```

5. Now you can use `gitt` in any Git Bash terminal!

#### Option 2: WSL (Windows Subsystem for Linux)

1. Install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) (Windows 10/11)
   ```powershell
   wsl --install
   ```

2. Open your WSL terminal and follow the **macOS / Linux** instructions above

3. Use `gitt` in your WSL terminal

**Note:** Git Bash is recommended for most Windows users as it's simpler to set up and integrates well with Windows file systems.

## Usage

Navigate to any Git repository and run:

```bash
gitt
```

### Controls

- **↑/↓ Arrow Keys** - Navigate through files and menu options
- **Enter on a file** - Select/deselect that file (toggle checkbox)
- **Enter on Select All** - Select all files at once
- **Enter on Confirm** - Stage selected files and proceed to commit prompt

### Workflow Example

```
=== Interactive Git Add ===
Use ↑/↓ arrows to navigate, Enter to select/deselect

  [✓] M src/index.js
→ [ ] N src/utils.js
  [✓] M README.md

  [Select All]
  [Confirm and stage selected files]
```

After selecting files and confirming:
```
Successfully staged 2 file(s)!

=== Commit Changes ===
Use ↑/↓ to navigate, Enter to select

Commit message:
(empty - click 'Edit message' to add)

→ [Edit message]
  [Commit]
  [Skip - exit without committing]
```

Navigate with arrows and press Enter to edit the message, commit, or skip.

Status indicators:
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

- **Bash 3.2 or later**
  - macOS: Built-in (zsh/bash)
  - Linux: Built-in (bash)
  - Windows: Git Bash or WSL
- **Git** (version control system)
- **Terminal with ANSI color support** (most modern terminals)

## Why gitt?

The standard `git add` command requires you to type out file paths or use `git add -p` for interactive staging, which can be cumbersome. `gitt` provides a visual, checkbox-style interface that makes it easy to see all your changes and select exactly what you want to stage.

Additionally, `gitt` streamlines the commit workflow by optionally prompting for a commit message right after staging, eliminating the need to run separate `git add` and `git commit` commands.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details

## Author

Created by Liron Katsif
