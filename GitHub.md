# Introdução ao Git

### > O que é Git?

Sistema de controle de versão distribuído.

- Gratuito e openSource;

- Ramificação(branching) e fusões (merging) eficientes;

- Leve e rápido. 

- **O que é um commit? **

  "No mundo da programação, um commit é um ponto de salvamento permanente do seu projeto. Ele captura o estado exato de todos os seus arquivos naquele momento."

- **O que é um Branching?**

  "Em resumo: Branching é como criar uma realidade alternativa para o seu projeto, onde você pode fazer mudanças e experimentos sem medo de quebrar a versão oficial. Quando a sua "realidade alternativa" estiver pronta e funcionando, você pode uni-la à principal."

### > Breve histórico do Git

O projeto do núcleo (Kernel) do linux, que é open source, começa a ultilizar o BitKeeper, um DVCS proprietário;

### > Versionamento de Código :

A cada alteração do meu código eu gero uma nova versão.

**Sistemas de Controle de Versão**

 Controlam as versões de um arquivo ao longo do tempo. Registra o histórico das versões modificadas

**VCS Distribuído** = Clona um repositório completo, o que inclui o histórico de versões.

###  > Comando Básicos para Linux:

- ls = Mostrar a lista de diretórios;
- mkdir = Criar pastas;
- rm -rf = Apagar diretórios/Arquivos
- cd Entrar/Navegar entre as pastas 

#  Configuração Inicial do Git

Antes de tudo, configure seu nome de usuário e e-mail. Eles serão associados aos seus commits.

Abra o terminal e execute os seguintes comandos:

- git config --global user.name "Ricardo"
- git config --global user.email "ricardo@gmail.com"



# Subir um Projeto Local para o GitHub

**Navegue até a pasta do seu projeto**:

- cd /home/ricardo/Estudos

**Inicialize o repositório Git**:

- git init

**Adicione o repositório remoto**: Crie um novo repositório no site do GitHub e copie a URL. Em seguida, execute o comando abaixo:

- git remote add origin https://github.com/ricardodev/meu-projeto.git

**Adicione os arquivos** para o controle de versão e faça o commit:

- git add .
- git commit -m "Primeiro commit"

**Defina a branch principal** e envie os arquivos:

- git branch -M main
- git push -u origin main

#  Clonar e Atualizar um Projeto Existente

1. **Clone o repositório**: Navegue até o diretório onde deseja salvar o projeto e execute:

- cd C:\\Users\\Seu Nome\\Documents
- git clone https://github.com/ricardodev/meu-projeto.git

2. **Para enviar alterações**, use os comandos padrão:

- git add .
- git commit -m "Alterações feitas no trabalho"
- git push

3. **Para baixar atualizações** feitas por outros colaboradores ou de outro local, utilize:

- git pull
.
