# Instalar e configurar wsl com debian 10 no Windows 10

👋 Bem vindo, iremos deixar seu windows um pouco menos ruim!

Passos a serem seguidos

- [x]  Ter windows instalado
- [ ]  Abra o PowerShell em Administrador, e execute o seguinte comando:

        Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

    > Caso solicite, reinicie o PC.

- [ ]  Abra a Microsoft Store. Pesquise por Debian.
- [ ]  Após a instalação abra o Debian e insira o seu nome de usuário e senha. (não precisa ser a mesma do windows).
- [ ]  rode o comando para a atualizar o sistema. (ele irá pedir a sua senha que você definiu para o Debian).

        sudo apt update && sudo apt upgrade

- [ ]  Após isso instale o git.

        sudo apt install git

- [ ]  pesquise na barra de pesquisa do windows por, substituido o "user" pelo nome do seu usuário do Debian.

        \\wsl$\Debian\home\"user"

- [ ]  Depois abra o diretório e arraste para o acesso rápido do Windows