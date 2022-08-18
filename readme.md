## Descrição

    Este repositório tem como objetivo apenas armazenar as inforamações de forma prática de como utilizar os comandos e controle de versionamento do Git.

## Instalação e configuração

1º passo : fazer o dowload do git: link [aqui](https://git-scm.com/downloads)!

2º passo: configuração de forma global para poder fazer os commits, configurar o nome:

    git config --global user.name "Cléo Constantino"

3º passo: configurar o e-mail: (o e-mail deve ser o mesmo do cadastro do github, se não não vai vincular ao perfil do git):

    git config --global user.email "cleoconstantino@outlook.com"


## Comandos

Criar uma pasta:

    mkdir projetogit

Entrar na pasta:

    cd projetogit

Listar os arquivos dentro da pasta:

    ls

Iniciar um projeto git: (ele vai iniciar um repositório git vazio, na pasta que está dentro. Ele cria uma branch - vai estar na master)

    git init

Se der o comando 'ls' vai mostrar a pasta vazia, mas tem um arquivo oculto, onde se der o comando 'ls -a' vai mostrar o arquivo. 

Mostrar o estado de cada arquivo dentro da pasta:

    git status
    ** os arquivos dentro de 'Untracked files:' 
    são os arquivos que ainda não estão sendo versionados pelo git

Para adicionar, por exemplo, apenas um arquivo, dar o comando:

    git add nomedoarquivo

Ao dar uma 'git status' novamente, o arquivo vai aparecer em 'Changes to be committed' > alterações para serem comitadas.

Verificar os commits já feitos:

    git log

Limpar o terminal:


    Ctrl + L

Adicionar todos os arquivos da pasta:


    git add .

Fazer commit com a mensagem direta:


    git commit -m "Mensagem aqui"

Sair da tela: pressionar a letra 'Q'

Verificar as informações de um arquivo alterado:

    git diff nomedoarquivo

Remover uma pasta:

    rm -rf nomedapasta

Verificar a branch que está sendo usada:

    git branch

Mudar a branch:

    git branch -M "nome-da-branch"

## Enviar os commits para o GitHub

Criar um repositório o github e fazer algumas configurações de SSH (a chave 'publica' é configurada no github, e a chave privada fica no computador).

Passo a passo:
Fazer o login no GitHub > Perfil > Settings > SSH and GPG keys > New SSH key > Colocar um titulo > e na caixa 'Key' colocar a chave pública.

Para gerar a chave pública:
Abrir o terminal,  dar o comando:

    ssh-keygen

Após esse comando, o ternimal pergunta se quer colocar um nome na chave, se não quiser é só apertar enter. Em seguida vai perguntar se deseja colocar uma senha, para deixar vazio é só dar enter. Ao dar o comando 'ls', vai mostrar os arquivos criados, e o arquivo com a extensão '.pub' é a chave pública criada.

Para acessar a chave, deve estar na pasta onde a chave foi criada e dar o comando abaixo:

    cat nomedoarquivo.pub

Copiar a chave;
 
Para congigurar a chave SSH no conmputador deve-se rodar mais dois comandos:

    eval `ssh-agent`
    ssh-add nome-da-ssh-privada

No GitHub > colar a chave copiada anteriormente e clicar em 'Add SSH key';

Agora criar um repositório > ao criar o git já vai sugerir os comandos quando o repositório já está criado(dar o comando dentro da pasta que você quer conectar com o Git):

    git remote add origin colar-o-caminho-do-repositorio
    git push origin master


## Projeto alterado no Git e atualizar no computador

Baixar os aquivos alterados:

    git pull origin master

Deipois de baixar, para mostrar as informações dentro do arquivo:

    cat nome-do-arquivo

## Baixar um projeto do GitHub no computador

Pra copiar um projeto do github: clica no botão 'Code' > na aba SSH copia o código > no terminal, digitar: 

    git clone linkcopiado

## Comandos básicos do dia a dia 

    git add .
    git commit -m "Mensagem"
    git push origin master

Para saber mais sobre os status, acessar [esse link](https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio).