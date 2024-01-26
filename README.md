**How to install dotfiles**
========

1. Clone git repository - git clone https://github.com/pibarull/dotfiles.git
2. Install Homebrew: - /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" 
- Run these two commands in your terminal to add Homebrew to your PATH: 
  1) (echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/iliaershov/.zprofile 
  2) eval "$(/opt/homebrew/bin/brew shellenv)"
3. Download python - Search and select version 
- brew search python 
- Install - `brew install python@3.10` OR `brew install python` 
**HINT**: Better install latest python with `brew install python`, otherwise check https://stackoverflow.com/questions/71468590/env-python-no-such-file-or-directory-when-building-app-with-xcode
4. Install On-my-zsh - `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
5. In case if dotfile repo’s submodules are outdated, you need to: 
- cd [Outdated submodule] 
- checkout to the latest commit/release 
- git submodule update --init --recursive 
- commit changes
- run `cd ..` and `./install` 
You may need to comment `git submodule update --init --recursive "${DOTBOT_DIR}»` line in `install` script and update submodules manually.
7. If «~/.zshrc already exists but is a regular file or directory» error occures ->  rm ~/.zshrc ./install

