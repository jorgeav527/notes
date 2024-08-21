## Basic
1. Installing basic package
    - `sudo apt update && sudo apt install build-essential`
2. Installing [zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
    - `sudo apt install zsh`
    - Install ohmyzsh (MP!)
    - `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
3. Installing [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on debian 12
    - `sudo apt install git-all`
    - configuring git
        - `git config --global user.name "github-user"`
        - `git config --global user.email “your_email_from_github@example.com`
    - setup a [ssh-keygen](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
      - `ssh-keygen -t ed25519 -C "your_email@example.com"`
      - `eval "$(ssh-agent -s)"`
      - `ssh-add ~/.ssh/id_ed25519`
4. Install others packages
    - [Brave](https://brave.com/linux/)
      - `sudo apt install curl`
      - `sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg`
      - `echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list`
      - `sudo apt update`
      - `sudo apt install brave-browser`
    - Discord
      - First download the last version of the .deb package [here](https://discord.com/download?linux)
      - `sudo dpkg -i discord-*.*.*.deb`
    - Mongo Compas
    - Redis Insight
    - VSCode
    - Obsidian
    - ZED
