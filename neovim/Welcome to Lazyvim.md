This will be the instructions to install [lazyvim](https://www.lazyvim.org/) on Debian 12

## Requirements

***"The actual release  version is 0.10.0"***
1. Install Neovim >= **0.9.0** (needs to be built with **LuaJIT**):
	- First go to the [releases pages](https://github.com/neovim/neovim/releases/tag/v0.10.0)
	- Download [nvim-linux64.tar.gz](https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz) `curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz`
	- Delete old installation `sudo rm -rf /opt/nvim` 
	- Extract `sudo tar -C /opt -xzf nvim-linux64.tar.gz`
	- Add to the zsh path `echo 'export PATH="$PATH:/opt/nvim-linux64/bin"' >> ~/.zshrc`
	- Source the .zshrc file to refresh the terminal `source ~/.zshrc`
	- Run `nvim`
2. Install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on debian 12 `sudo apt install git-all`
3. Install some NerdFont I like [HackNerdFontMono](https://github.com/ryanoasis/nerd-fonts/blob/master/patched-fonts/Hack/Regular/HackNerdFontMono-Regular.ttf)
4. Manual Installation of [lazygit](https://github.com/jesseduffield/lazygit)  
	- *You'll need to have Go installed on your system* 
	- Clone the Repository: `git clone https://github.com/jesseduffield/lazygit.git`
	- `cd lazygit`
	- `go install`
	- `lazygit --version`
5. I have to install a **C** compiler for `nvim-treesitter` `cargo install tree-sitter-cli` because of this post [nvim-treesitter/issues/1097](https://github.com/nvim-treesitter/nvim-treesitter/issues/1097)
6. To install  [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
   - First install [ripgrep](https://github.com/BurntSushi/ripgrep) `cargo install ripgrep`
   - Second [fd](https://github.com/sharkdp/fd) `cargo install fd-find`
7. I choose the [alacritty](https://github.com/alacritty/alacritty):
	- `git clone https://github.com/alacritty/alacritty.git && cd alacritty`
	- Update the rust `rustup override set stable && rustup update stable`
	- Install debian 12 dependencies `sudo apt install cmake pkg-config libfreetype6-dev libfontconfig1-dev libxcb-xfixes0-dev libxkbcommon-dev python3`
	-  `cargo build --release` I'm using discord so I have a config file to disable Wayland (Force support for only X11), you can build it with `cargo build --release --no-default-features --features=x11`
	- if when running this command every thing is good `infocmp alacritty` and the response is somethis like this at the end  `...tsl=\E]2;, u6=\E[%i%d;%dR, u7=\E[6n,u8=\E[?%[;0123456789]c, u9=\E[c, vpa=\E[%i%p1%dd,`
	- To configure the program to be accessible in the Debian desktop run the following commands
		- `sudo cp target/release/alacritty /usr/local/bin`
		- `sudo cp extra/logo/alacritty-term.svg /usr/share/pixmaps/Alacritty.svg`
		- `sudo desktop-file-install extra/linux/Alacritty.desktop`
		- `sudo update-desktop-database`
		- *if you want to [configure your alacritty](https://alacritty.org/config-alacritty.html) terminal you have to create a alacritty.toml file in `$HOME/.config/alacritty/alacritty.toml`*
    - This is the configuration I'm using:
    ```toml
    [window]
    startup_mode = "Maximized"  # Default: "Windowed"

    [font]
    normal = { family = "Hack Nerd Font Mono", style = "Regular" }  # Default for Linux/BSD: "monospace", Regular
    bold = { family = "Hack Nerd Font Mono", style = "Bold" }  # Inherits family from normal, Default style: Bold
    italic = { family = "Hack Nerd Font Mono", style = "Italic" }  # Inherits family from normal, Default style: Italic
    bold_italic = { family = "Hack Nerd Font Mono", style = "Bold Italic" }  # Inherits family from normal, Default style: Bold Italic
    size = 12.25  # Default: 11.25

    [cursor]
    style = { shape = "Block", blinking = "On" }  # Default: shape = "Block", blinking = "Off"
    ```
	- Clone the starter `git clone https://github.com/LazyVim/starter ~/.config/nvim`
	- and after just run `nvim`
