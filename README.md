# My-Terminal

- 해당 레포지토리는 `mac`, `linux`, `windows`에서 터미널 환경을 사용할때마다 번거로움을 느껴 설정 커맨드를 저장하고자 하는 레포지토리입니다.

- Windows
   ![windows](./imgs/win.png)

- Mac
   ![Macs](./imgs/mac.png) 

## Mac,Linux

- `mac`은 기본적으로 `brew`가 필요합니다.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

   ![mac1](./imgs/mac1.png)

- 'brew'가 설치 되었다면 `mac`에서 다양한 기능을 가진 터미널 `Iterm2`를 설치해보도록 하겠습니다.


```bash
Iterm2

brew install --cask iterm2

```
   ![mac2](./imgs/mac2.png)
   - 왼쪽 `iterm` 오른쪽 `Terminal`   

- 저는 `bash` 보다 `zsh`환경을 선호하는 편이기 때문에 `zsh`도 설치하겠습니다.   

```bash
# curl 사용하여 zsh 설치
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
   ![mac3](./imgs/mac3.png)

```bash
# zsh 플러그인 Auto Suggestions
brew install zsh-autosuggestions

# Auto Suggestions 세팅
echo "source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc

# zsh플러그인 Syntax Highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Syntax Highlighting 세팅
echo "source ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${HOME}/.zshrc

# zsh 테마 Powerlever10k 설치
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

```
| zsh-autosuggestions | zsh-syntax-highlighting | 
|-------------- | -------------- | 
| ![mac4](./imgs/mac4.png)|![mac5](./imgs/mac5.png)|


- 해당 설치 과정을 수행하고 나고 `zsh`를 타이핑 하면 `powerlevel10k`의 세팅 화면이 시작 될것입니다.

> Powerlever10k는 `Nerd Font`가 없으면 아이콘이 깨지게 되기 때문에 저는 `Fira Code Nerd Font`를 설치해서 사용했습니다  
>
> [Nerd Font](https://www.nerdfonts.com/font-downloads) 

- 마지막으로 `IDE Neovim`과 `Github TUI Tool lazygit`을 설치하면 끝입니다.  

```bash
# neovim 설치
brew install neovim

# neovim 커스텀 세팅
git clone https://github.com/kimud6003/NvChad ~/.config/nvim; nvim

# lazygit 설치
brew install lazygit
```
   ![mac6](./imgs/mac6.png)
   - vim vs Neovim

   ![mac7](./imgs/mac7.png)
   - lazygit
## Window
