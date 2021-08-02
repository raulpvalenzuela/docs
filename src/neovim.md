# Neovim

## Neovim Installation

### Package installation

1. Installation:

   ```bash
   sudo pacman -S neovim
   ```

## Color schemes

Themes come in the form of `.vim` files.

### Manual installation

1. Create `colors` folder if missing:

   ```bash
   mkdir ~/.config/nvim/colors
   ```

2. Copy `.vim` file into `colors` folder:

   ```bash
   cp theme.vim ~/.config/nvim/colors
   ```

3. Add this line to the `~/.config/nvim/init.vim` file or any sourced file from there:

   ```txt
   colorscheme theme.vim
   ```

## Collections of themes

- [https://github.com/rafi/awesome-vim-colorschemes](https://github.com/rafi/awesome-vim-colorschemes)
- [https://github.com/mcchrish/vim-no-color-collections](https://github.com/mcchrish/vim-no-color-collections)
- [https://github.com/rainglow/vim](https://github.com/rainglow/vim)
- [https://github.com/nightsense/vimspectr](https://github.com/nightsense/vimspectr)
- [https://github.com/chriskempson/base16-vim](https://github.com/chriskempson/base16-vim)
- [https://github.com/mswift42/vim-themes](https://github.com/mswift42/vim-themes)
- [https://github.com/mkarmona/colorsbox](https://github.com/mkarmona/colorsbox)

## Plugin manager vim-plug

### Links

- [https://github.com/junegunn/vim-plug](https://github.com/junegunn/vim-plug)
- [https://www.chrisatmachine.com/Neovim/01-vim-plug/](https://www.chrisatmachine.com/Neovim/01-vim-plug/)

Although there is the possibility to manually install plugins in neovim, it is much easier to maintain those plugins with the use of a plugin manager. This way, the plugins themselves do not need to be included in the dotfiles repository, as the plugin manager download them to the configured path on demand.

### vim-plug installation

```bash
curl -fLo ~/.config/nvim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### vim-plug usage

1. Begin the section with call plug#begin()
2. List the plugins with Plug commands
3. End the section with call plug#end()
4. Reload `/init.vim` and execute `:PlugInstall` to install plugins.

Example:

```vim
call plug#begin('~/.config/nvim/autoload/plugged')

Plug 'vim-airline/vim-airline'

call plug#end()
```

## Usage

### Links

- Neovim man pages
- [https://devhints.io/vim](https://devhints.io/vim)
- [https://linux.com/training-tutorials/vim-101-beginners-guide-vim](https://linux.com/training-tutorials/vim-101-beginners-guide-vim)

### Opening file(s) in Neovim

The regular way of openin one or more files in Neovim is:

```bash
nvim {file1} {file2}...
```

This are some of the most common and useful modifiers that can be added when opening files:

| Shortcut                | Description                                    |
| ----------------------- | ---------------------------------------------- |
| `-d {file1} {file2}...` | Open in diff mode up to 4 files                |
| `-p {file1} {file2}...` | Open each file in tabs                         |
| `-o {file1} {file2}...` | Open each file in windows stacked horizontally |
| `-O {file1} {file2}...` | Open each file in windows stacked vertically   |
| `-b`                    | Open in binary mode                            |

### Exiting

| Shortcut   | Description                      |
| ---------- | -------------------------------- |
| `:qa`      | Close all files                  |
| `:qa!`     | Close all files, abandon changes |
| `:w`       | Save                             |
| `:wq / :x` | Save and close file              |
| `:q`       | Close file                       |
| `:q!`      | Close file, abandon changes      |
| `ZZ`       | Save and quit                    |
| `ZQ`       | Quit without checking changes    |

### Navigating

- General

| Shortcut          | Description       |
| ----------------- | ----------------- |
| `h j k l`         | Arrow keys        |
| `\<C-U> / \<C-D>` | Half-page up/down |
| `\<C-B> / \<C-F>` | Page up/down      |

- Words

| Shortcut | Description               |
| -------- | ------------------------- |
| `b / w`  | Previous/next word        |
| `ge / e` | Previous/next end of word |

- Line

| Shortcut | Description                      |
| -------- | -------------------------------- |
| `0`      | Start of line                    |
| `^`      | Start of line (after whitespace) |
| `$`      | End of line                      |

- Character

| Shortcut | Description                |
| -------- | -------------------------- |
| `fc`     | Go forward to character c  |
| `Fc`     | Go backward to character c |

- Document

| Shortcut | Description  |
| -------- | ------------ |
| `gg`     | First line   |
| `G`      | Last line    |
| `:n`     | Go to line n |
| `nG`     | Go to line n |

- Window

| Shortcut | Description              |
| -------- | ------------------------ |
| `zz`     | Center this line         |
| `zt`     | Top this line            |
| `zb`     | Bottom this line         |
| `H`      | Move to top of screen    |
| `M`      | Move to middle of screen |
| `L`      | Move to bottom of screen |

- Search

| Shortcut | Description                      |
| -------- | -------------------------------- |
| `n`      | Next matching search pattern     |
| `N`      | Previous match                   |
| `\`      | * Next whole word under cursor   |
| `#`      | Previous whole word under cursor |

### Editing

| Shortcut  | Description                         |
| --------- | ----------------------------------- |
| `a`       | Append                              |
| `A`       | Append from end of line             |
| `i`       | Insert                              |
| `o`       | Next line                           |
| `O`       | Previous line                       |
| `s`       | Delete char and insert              |
| `S`       | Delete line and insert              |
| `C`       | Delete until end of line and insert |
| `r`       | Replace one character               |
| `R`       | Enter Replace mode                  |
| `u`       | Undo changes                        |
| `\<C-R\>` | Redo changes                        |

### Clipboard

| Shortcut    | Description                 |
| ----------- | --------------------------- |
| `x`         | Delete character            |
| `dd`        | Delete line (Cut)           |
| `yy`        | Yank line (Copy)            |
| `p`         | Paste                       |
| `P`         | Paste before                |
| `"*p / "+p` | Paste from system clipboard |
| `"*y / "+y` | Paste to system clipboard   |

### Diff mode

- Navigating

| Shortcut   | Description                 |
| ---------- | --------------------------- |
| `CTRL + w` | Switch between diff windows |
| `]c`       | Next difference             |
| `[c`       | Previous difference         |

- Editing

| Shortcut      | Description                                       |
| ------------- | ------------------------------------------------- |
| `do`          | Diff Obtain! Pull the changes to the current file |
| `dp`          | Diff Put! Push the changes to the other file      |
| `:diffupdate` | Re-scan the files for differences                 |
| `ZQ`          | Quit without checking changes                     |

### Operators list

| Shortcut | Description                     |
| -------- | ------------------------------- |
| `d`      | Delete                          |
| `y`      | Yank (copy)                     |
| `c`      | Change (delete then insert)     |
| `>`      | Indent right                    |
| `<`      | Indent left                     |
| `=`      | Autoindent                      |
| `g~`     | Swap case                       |
| `gU`     | Uppercase                       |
| `gu`     | Lowercase                       |
| `!`      | Filter through external program |

### Text objects

| Shortcut    | Description              |
| ----------- | ------------------------ |
| `p`         | Paragraph                |
| `w`         | Word                     |
| `s`         | Sentence                 |
| `[ ( { <`   | A [], (), {} or <> block |
| `` ' " ` `` | A quoted string          |
| `b`         | A block [(               |
| `B`         | A block in [{            |
| `t`         | A XML tag block          |

### Commands

| Shortcut                       | Description                                                                                             |
| ------------------------------ | ------------------------------------------------------------------------------------------------------- |
| `:e file`                      | Start editing a new file                                                                                |
| `:r file`                      | Read contents of a file to the workspace                                                                |
| `/text`                        | Search for `text` in the document, going forward.                                                       |
| `?text`                        | Search for `text` in the document, going backwards.                                                     |
| `:%s/text/replacement text/g`  | Search through the entire document for `text` and replace it with `replacement text`                    |
| `:s/text/replacement text/g`   | Same as above but in the current line instead of the entire document                                    |
| `:%s/text/replacement text/gc` | Search through the entire document and confirm before replacing text                                    |
| `:s/text/replacement text/gc`  | Same as above but in the current line instead of the entire document                                    |
| `:%s/text/replacement text/gi` | Search through the entire document for `text` (case insensitive) and replace it with `replacement text` |
| `:s/text/replacement text/gi`  | Same as above but in the current line instead of the entire document                                    |
| `.`                            | Repeat last command                                                                                     |
