# Development Configuration Files

This folder contains configuration files for development tools optimized for Flutter and Python development.

## Files

- **`.tmux.conf`** - Tmux configuration with mouse support, custom key bindings, and vi mode
- **`.vimrc_flutter`** - Vim configuration optimized for Flutter/Dart development
- **`.vimrc_python`** - Vim configuration optimized for Python development (PEP 8 compliant)

## Installation

### Tmux Configuration
```bash
# Copy to home directory
cp ~/configs/.tmux.conf ~/.tmux.conf

# Reload tmux configuration (if tmux is already running)
tmux source-file ~/.tmux.conf
```

### Vim Configuration for Flutter
```bash
# Option 1: Use as main vimrc
cp ~/configs/.vimrc_flutter ~/.vimrc

# Option 2: Source it from your existing vimrc
echo "source ~/configs/.vimrc_flutter" >> ~/.vimrc
```

### Vim Configuration for Python
```bash
# Option 1: Use as main vimrc
cp ~/configs/.vimrc_python ~/.vimrc

# Option 2: Source it from your existing vimrc
echo "source ~/configs/.vimrc_python" >> ~/.vimrc
```

## Features

### Tmux Configuration
- **Prefix Key**: Changed from `Ctrl+b` to `Ctrl+a`
- **Mouse Support**: Enabled for easier navigation
- **Split Panes**: 
  - `|` for horizontal split
  - `-` for vertical split
- **Navigation**: Alt+Arrow keys to switch between panes
- **Vi Mode**: Enabled for copy mode
- **Reload Config**: `Prefix + r` to reload configuration
- **Enhanced Status Bar**: Shows date and time
- **256 Color Support**: Better syntax highlighting

### Vim Configuration (Flutter)
- **Indentation**: 2 spaces for Dart and YAML files
- **Line Numbers**: Absolute and relative
- **Leader Key**: `,` (comma)
- **Flutter Shortcuts**:
  - `,fr` - Flutter run
  - `,ft` - Flutter test
  - `,fb` - Flutter build APK
  - `,fd` - Flutter doctor
  - `,fp` - Flutter pub get
  - `,fc` - Flutter clean
- **Auto-pairs**: Automatic bracket and quote closing
- **Split Navigation**: `Ctrl+h/j/k/l` for moving between splits
- **Code Folding**: `Space` to toggle folds

### Vim Configuration (Python)
- **Indentation**: 4 spaces (PEP 8 compliant)
- **Line Numbers**: Absolute and relative
- **Leader Key**: `,` (comma)
- **Python Shortcuts**:
  - `,r` - Run current Python file
  - `,t` - Run pytest
  - `,l` - Run pylint on current file
  - `,f` - Format with black
  - `,i` - Sort imports with isort
- **Whitespace Highlighting**: Trailing whitespace highlighted in red
- **Auto-pairs**: Automatic bracket and quote closing
- **Split Navigation**: `Ctrl+h/j/k/l` for moving between splits
- **Code Folding**: `Space` to toggle folds
- **Virtual Environment**: Automatic detection and support
- **Abbreviations**:
  - `pdb` - Insert pdb breakpoint
  - `ifmain` - Insert if __name__ == '__main__'

## Common Key Bindings

### Both Vim Configurations
- `,w` - Save file
- `,q` - Quit
- `,<space>` - Clear search highlight
- `Ctrl+h/j/k/l` - Navigate between splits
- `Space` - Toggle code folding

## Prerequisites

### For Vim Undo Feature
```bash
mkdir -p ~/.vim/undo
```

### For Python Virtual Environment Support
Make sure you have Python 3 with vim support:
```bash
vim --version | grep python3
```

## Customization

Feel free to modify these configurations to suit your preferences. Each configuration file is well-commented to help you understand and customize settings.
