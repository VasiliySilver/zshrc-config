# Simple ZSH Configuration Setup

### Step 1: Download the .zshrc File

1. Open your terminal.
2. Navigate to your home directory:
   ```
   cd ~
   ```
3. Download the .zshrc file using the curl command:
   ```
   curl -o .zshrc https://raw.githubusercontent.com/VasiliySilver/zshrc-config/main/.zshrc
   ```
   This will download the .zshrc file from the GitHub repository and save it in your home directory.

### Step 2: Install Dependencies

#### Install Neovim (nvim)

1. Install Neovim using your package manager. For example, on macOS with Homebrew:
   ```
   brew install neovim
   ```
   On Ubuntu:
   ```
   sudo apt-get install neovim
   ```

#### Install pyenv

1. Install pyenv using the following command:
   ```
   curl https://pyenv.run | bash
   ```

#### Install zoxide

1. Install zoxide using the following command:
   ```
   cargo install zoxide
   ```

#### Install Zinit

1. Install Zinit using the following command:
   ```
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma-continuum/zinit/master/install.sh)"
   ```

#### Install Other Dependencies

1. Install the additional dependencies (pyenv-virtualenv, zsh-autosuggestions, zsh-syntax-highlighting) using your package manager. For example, on macOS with Homebrew:
   ```
   brew install pyenv-virtualenv zsh-autosuggestions zsh-syntax-highlighting
   ```
   On Ubuntu:
   ```
   sudo apt-get install pyenv-virtualenv zsh-autosuggestions zsh-syntax-highlighting
   ```

### Step 3: Reload the ZSH Configuration

1. Reload your ZSH configuration:
   ```
   source ~/.zshrc
   ```

That's it! Your ZSH configuration is now set up, and the necessary dependencies are installed.

Remember, if you encounter any issues or need further assistance, don't hesitate to refer to the documentation of the specific dependencies or seek help from the respective communities.

Let me know if you have any other questions!
