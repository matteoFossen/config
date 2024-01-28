<!-- README -->

# LE MIE CONFIGURAZIONI

> **DISCLAIMER**
> Tutte le mie configurazioni considerano il clone di questo repository già effettuato.
> ```bash
> git clone https://github.com/matteoFossen/dotfiles.git
> ```


### Essenziali

```bash
sudo apt install git htop btop bmon openssl tldr net-tools build-essential
tldr -u
mkdir $HOME/GIT
```

### JetBrains Mono Font

```bash
curl -fsSL https://raw.githubusercontent.com/JetBrains/JetBrainsMono/master/install_manual.sh | bash -c
```

> Impostare il font `JetBrains Mono` in tutte le varie configurazioni per applicarlo.

### Sfondi

```bash
git clone https://github.com/D3Ext/aesthetic-wallpapers.git wallpapers
mkdir -p $HOME/.config/wallpaper
mv wallpapers/images $HOME/.config/wallpaper
rm -rf wallpapers
feh --bg-fill --randomize $HOME/.config/wallpaper/* &
```

### Terminale

Per impostare i colori del terminale seguire la guida di https://github.com/Gogh-Co/Gogh

### Tmux

Copia il contenuto del file `tmux.conf` in `$HOME/.config/tmux/tmux.conf`.

```bash
sudo apt install tmux
git clone https://github.com/tmux-plugins/tpm $HOME/.config/tmux/plugins/tpm
tmux
tmux source-file $HOME/.config/tmux/tmux.conf
```

Per finire `Ctrl+b I` installerà le estensioni di tpm in tmux.
Digitare `Ctrl+b r` per aggiornare le configurazioni correnti.

### ChatGPT

Seguire la giuda al link https://github.com/aandrew-me/tgpt  
Per dargli voce utilizzare https://github.com/rhasspy/piper  

> To do:  
> Aggiungere un programma che permette di ascoltare le istruzioni da dare a chatGPT  

### Zsh

```bash
sudo apt install zsh
echo "export ZSH_CUSTOM=$HOME/config/zsh/oh-my-zsh" >> $HOME/config/zsh/zshrc
chsh -s $(which zsh)
curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh | sh -c
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-$HOME/config/zsh/oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/config/zsh/oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/config/zsh/oh-my-zsh/custom}/themes/powerlevel10k
```
