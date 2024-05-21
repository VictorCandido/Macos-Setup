# Macos Setup

## Aplicativos
- Google Chrome
- Iterm2
- Visual Studio Code
- Alt-tab
- Spectacle
- Logitech Options
- Node

## Comandos
### Install Brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Zsh 
```
brew install zsh
```
```
chsh -s /usr/local/bin/zsh
```

### Oh My Zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
A partir de agora, todas as atualizações de código deverão ser adicionadas no arquivo `~/.zshrc`.

### Dracula Theme
```
git clone https://github.com/dracula/iterm.git
```
1. iTerm2 > Preferences > Profiles > Colors Tab
2. Open the Color Presets... drop-down in the bottom right corner
3. Select Import... from the list
4. Select the Dracula.itermcolors file
5. Select the Dracula from Color Presets...

### FiraCode
```
https://github.com/tonsky/FiraCode/releases
```

### Spaceship
```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```
```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```
Agora dentro do arquivo `~/.zshrc` vamos alterar a variável `ZSH_THEME` ficando dessa forma:
```
ZSH_THEME="spaceship"
```

### Plugins do ZSH
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"
```

Após essa instalação, vamos abrir o arquivo `~/.zshrc` novamente e abaixo da linha `### End of ZInit's installer chunk` que foi adicionada automaticamente no arquivo, adicionamos:

```
zinit light zdharma/fast-syntax-highlighting
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions
```

### Terminal no VSCode
Utilizar `Command + Shift + P` e pesquisar por `Preferences: Open Setting (JSON)`. Logo em seguida, adicionar a seguinte linha:
```
"terminal.integrated.shell.osx": "/bin/zsh"
```

## VSCode Plugins
- Dracula Official
- Material Icon Theme
- Angular Extension Pack
- Java Extension Pack
- GitLens — Git supercharged
- Live Server
- Beautify
- Live Share
