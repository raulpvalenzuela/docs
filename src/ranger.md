# Ranger

## Ranger installation

### Package installation

1. Installation:

   ```bash
   sudo pacman -S ranger
   ```

## Color schemes

Ranger comes with four color schemes: default, jungle, snow and solarized. You can change your color scheme in `~/.config/ranger/rc.conf` using:

```txt
set colorscheme scheme
```

Custom color schemes can be placed in `~/.config/ranger/colorschemes`.

## Plugins

Ranger has support for loading directories in the plugins folder.

To install a plugin place it in the plugins folder `~/.config/ranger/plugins`

### Plugin devicons

1. Install required NERDfont

   ```bash
   yay -S nerd-fonts-source-code-pro 
   ```

2. Clone the repository into ranger's plugins folder:

   ```bash
   git clone https://github.com/alexanderjeurissen/ranger_devicons ~/.config/ranger/plugins/ranger_devicons
   ```

3. Configure devicons in `~/.config/ranger/rc.conf` by adding this line:

   ```txt
   default_linemode devicons
   ```

## Usage

### Links

- 

