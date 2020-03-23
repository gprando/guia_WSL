# Configurando workspace

Agora vamos instalar tudo o que precisamos para desenvolver nossas aplicações.

- [ ]  Configurar o git (irei usar meus dados como exemplo, use os seus quando for fazer!):

        git config --global user.name Prando
        
        git config --global user.email gprando55@gmail.com
        
        git config --global color.ui true

- [ ]  Agora iremos criar uma chave ssh e adicionar em nossa conta do github/gitlab.

        ssh-keygen -t rsa -b 4096 -C gprando55@gmail.com  //vá dando enter até aparecer um quadrinho muito massa;
        
        eval "$(ssh-agent -s)"
        
        ssh-add ~/.ssh/id_rsa
        
        cat ~/.ssh/id_rsa.pub   //Copie a chave que aparecer no terminal, nas configurações do seu github

    > se tiver duvida, siga meu tutorial de git mais detalhado [https://github.com/gprando/guia_Git](https://github.com/gprando/guia_Git)

- [ ]  Agora basta Instalar o que precisamos, esse processo é um pouco chato, porém criei um script que tem boa parte do que uso, e creio que será suficiente para você também.

    [https://github.com/gprando/scripts](https://github.com/gprando/scripts)

    > clone e repositório e execute o script:

        git clone https://github.com/gprando/scripts
        
        cd scripts
        
        chmod +x *
        
        sudo ./configWSL.sh

    ## Agora é só ser feliz !