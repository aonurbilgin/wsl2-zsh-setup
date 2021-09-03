# Step 1: Install WSL2
Open windows powershell run as administrator then;
```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

## Enable Virtual Machine feature
```bash
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## Set WSL 2 as your default version
```bash
wsl --set-default-version 2
```
## Install your Linux distribution of choice

Open the Microsoft Store and select your favorite Linux distribution.


## Install Jetbrains Font
```bash
https://www.jetbrains.com/lp/mono/
```

# Step 2: Install oh-my-zsh
```bash
sudo apt install zsh
```
```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install useful plugins
[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

[powerlevel10k Theme](https://github.com/romkatv/powerlevel10k)
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

# Step 3: Configure ZSH
Open ~/.zshrc and modify its content like this:
```bash
# Use Powerlevel10k theme
ZSH_THEME="powerlevel10k/powerlevel10k"

# Use plugins
plugins=(docker zsh-autosuggestions zsh-syntax-highlighting)
```

After setting the theme, the Powerlevel10k wizard should show up, which will guide you through the setup. If it did not show up then try to run p10k configure.

More about [oh-my-zsh plugins](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) and [Powerlevel10k configuration](https://github.com/romkatv/powerlevel10k#configuration).