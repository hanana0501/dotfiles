## これはなに
vim初心者が最終的に全部をvimで開発するためのrepository  
C++,C#,ruby,markdown,json,swift,go,pythonに対応済み   

参考のakinama氏の[dotfiles](https://github.com/akinama/dotfiles)  

## 手順

setting.shで自動化したいけどまだできてないっ

- vimをいれる

```sh
$ cd
$ mkdir .dotfiles
$ cd .dotfiles
$ git clone git@github.com:hanana0501/dotfiles.git
$ sh setting.sh
$ brew install vim --with-client-server --with-lua
$ brew install the_silver_searcher
$ curl https://raw.githubusercontent.com/Shougo/neobundle.vim/master/bin/install.sh | sh
```

- antigenからzshのpluginを導入

```sh
$ cd
$ git clone https://github.com/zsh-users/antigen
$ source ~/.zshrc
```

- karabiner

```sh
$ brew install caskroom/cask/brew-cask
$ brew cask install karabiner
$ cd ~/Library/Application\ Support/Karabiner
$ rm private.xml
$ ln -s ~/.dotfiles/dotfiles/private.xml private.xml
```

karabinerを起動してLeave Insert Mode（以下略をONに

- tmux

```sh
$ brew install tmux
$ git clone https://github.com/erikw/tmux-powerline.git
$ gem install tmuxinator
```

- powerline

https://github.com/powerline/fonts
Hackのフォントを落としてインストールすること

http://mix-mplus-ipa.osdn.jp/migu/
Migu 1Mのフォントを落とそう

iTermでの設定はRegularはMigu1Mで16pt、NON-ASCIIはHackで18pt

```sh
$ git clone https://github.com/jeremyFreeAgent/oh-my-zsh-powerline-theme
$ cd oh-my-zsh-powerline-theme
$ ./install_in_omz.sh
```

## MEMO

- cocosを書く時は.ycm以下略のシンボリックリンクをcocosプロジェクトのトップに作ること

