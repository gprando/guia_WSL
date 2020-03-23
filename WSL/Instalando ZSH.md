# Instalando ZSH

Agora vamos deixar o terminal lindo, pois ninguém merece um workspace feio!!

- [ ]  No Debian digite (confirme tudo o que for sendo pedido):

        sudo apt-get install zsh

- [ ]  Instale o wget:

        sudo apt-get install wget

- [ ]  Abra o arquivo .bashrc no VS Code:

        code ~/.bashrc

- [ ]  Na primeira linha adicione, e depois salve e feche o editor:

        # if running in terminal...
        if test -t 1; then
        # ...start zsh
        exec zsh
        fi

- [ ]  Instale o curl:

        sudo apt install curl

# Agora vamos instalar o Oh My Zsh

- [ ]  Para instalar o oh my zsh

        sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

> A partir de agora todas configurações que você quer fazer como adicionar variáveis ambientes ou configurar seu terminal de qualquer forma utilize o arquivo ~/.zshrc e não mais o ~/.bash_profile ou derivados.

- [ ]  Reinicie seu terminal, e você verá algo diferente.

> Agora vamos instalar o tema drácula

    sudo apt-get install dconf-cli
    
    git clone https://github.com/dracula/gnome-terminal
    
    cd gnome-terminal
    
    ./install.sh

> Selecione 1,  depois YES, 2

# Agora vamos instalar o tema Spaceship

- [ ]  Instalando fonte fira code

https://github.com/tonsky/FiraCode/releases/download/2/FiraCode_2.zip

> Extrair e instalar todas as fontes dentro da pasta "ttf"

- [ ]  Agora ir em propriedades do Debian e mudar a fonte para "Fira code Retina"
- [ ]  Agora instalando tema Spaceship

        cd
        
        git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
        
        ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

- [ ]  Agora dentro do arquivo ~/.zshrc vamos alterar a variável ZSH_THEME ficando dessa forma(Abra o arquivo com [  code ~/.zshrc  ]):

        ZSH_THEME="spaceship"

    > Reinicie o Debian.

- [ ]  No fim do arquivo ~/.zshrc adiciono o seguinte conteúdo:

        SPACESHIP_PROMPT_ORDER=(
          user          # Username section
          dir           # Current directory section
          host          # Hostname section
          git           # Git section (git_branch + git_status)
          hg            # Mercurial section (hg_branch  + hg_status)
          exec_time     # Execution time
          line_sep      # Line break
          vi_mode       # Vi-mode indicator
          jobs          # Background jobs indicator
          exit_code     # Exit code section
          char          # Prompt character
        )
        SPACESHIP_USER_SHOW=always
        SPACESHIP_PROMPT_ADD_NEWLINE=false
        SPACESHIP_CHAR_SYMBOL="❯"
        SPACESHIP_CHAR_SUFFIX=" "

# Instalando plugins

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"

- [ ]  No fim do arquivo ~/.zshrc adiciono o seguinte conteúdo:

        zinit light zdharma/fast-syntax-highlighting
        zinit light zsh-users/zsh-autosuggestions
        zinit light zsh-users/zsh-completions

> Após isso reinicie o Debian

Tutorial seguido e adaptado para nossa realidade:

[https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/](https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/)