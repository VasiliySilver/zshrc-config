## Comprehensive ZSH and Program Setup

### Step 1: Install ZSH and Oh-My-ZSH

1. Open your terminal.
2. Install ZSH (Z Shell) using your package manager. For example, on Ubuntu:
   ```
   sudo apt-get install zsh
   ```
3. Install Oh-My-ZSH, a popular framework for managing your ZSH configuration:
   ```
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```
4. Set ZSH as your default shell:
   ```
   chsh -s $(which zsh)
   ```

### Step 2: Configure ZSH

1. Open your ZSH configuration file:
   ```
   nano ~/.zshrc
   ```
2. Customize your ZSH configuration by adding plugins, themes, and other settings. For example, you can uncomment or add the following lines:
   ```
   # Add Powerlevel10k theme
   zinit ice deph=1; zinit light romkatv/powerlevel10k;

   # Add ZSH plugins
   zinit light zsh-users/zsh-syntax-highlighting
   zinit light zsh-users/zsh-completions
   zinit light zsh-users/zsh-autosuggestions
   zinit light Aloxaf/fzf-tab
   ```
3. Save the changes and exit the text editor.
4. Reload your ZSH configuration:
   ```
   source ~/.zshrc
   ```

Step 3: Install Neovim (nvim) and Your Custom Configuration
Install Neovim using your package manager. For example, on Ubuntu:
sudo apt-get install neovim git

Clone your custom Neovim configuration repository:
git clone https://github.com/VasiliySilver/nvim.nchad.git ~/.config/nvim

Reload your ZSH configuration:
source ~/.zshrc

### Step 4: Download and Install the MesloLGS NF Fonts
Download the required font files from the provided URLs:
wget https://github.com/VasiliySilver/zshrc-config/blob/main/MesloLGS%20NF%20Bold%20Italic.ttf
wget https://github.com/VasiliySilver/zshrc-config/blob/main/MesloLGS%20NF%20Bold.ttf
wget https://github.com/VasiliySilver/zshrc-config/blob/main/MesloLGS%20NF%20Italic.ttf
wget https://github.com/VasiliySilver/zshrc-config/blob/main/MesloLGS%20NF%20Regular.ttf

Install the downloaded font files on your Ubuntu system. You can do this by double-clicking each font file and following the on-screen instructions to install them.

### Step 5: Change the Terminal Font
1. Open your terminal emulator (e.g., GNOME Terminal, Konsole, etc.).
2. Go to the settings or preferences of your terminal.
3. Locate the "Font" or "Text" settings.
4. Select the "MesloLGS NF" font family.
5. Apply the changes and close the terminal settings.

### Step 6: Install pyenv and pyenv-virtualenv

1. Install the necessary dependencies for pyenv:
   ```
   sudo apt-get install -y build-essential libssl-dev zlib1g-dev \
       libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
       libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev \
       git mc
   ```
2. Install pyenv:
   ```
   curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
   ```
3. Add the following lines to your `.zshrc` file to initialize pyenv:
   ```
   echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/.zshrc
   echo 'eval "$(pyenv init --path)"' >> ~/.zshrc
   echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc
   ```
4. Reload your ZSH configuration:
   ```
   source ~/.zshrc
   ```
5. Install the pyenv-virtualenv plugin:
   ```
   git clone https://github.com/pyenv/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv
   ```
6. Add the following line to your `.zshrc` file to enable the pyenv-virtualenv plugin:
   ```
   echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc
   ```
7. Reload your ZSH configuration:
   ```
   source ~/.zshrc
   ```

### Step 7: Install zoxide

1. Install zoxide, a fast alternative to the built-in `cd` command:
   ```
   sudo apt install install zoxide
   ```
2. Add the following line to your `.zshrc` file to initialize zoxide:
   ```
   source <(zoxide init zsh)
   ```
3. Reload your ZSH configuration:
   ```
   source ~/.zshrc
   ```

### Step 8: Install NVM (Node Version Manager)

1. Install NVM using the following commands:
   ```
   # For zsh
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | zsh
   source ~/.zshrc
   # For Bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
   source ~/.bashrc
   ```

If you encounter any issues or need additional assistance, don't hesitate to refer to the documentation of the specific tools or seek help from the respective communities.
