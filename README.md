# OmniStack-9

<p align="center">
  <img src="./readme/logo.svg" alt="Logo" width="300"/>
  <br>
</p>
<h3 align="center">
Uma espécie de "Tinder" para os Devs.
</h3>

<br><br>

<p align="center">
  <img src="https://img.shields.io/static/v1?label=Omnistack&message=9&color=blueviolet&style=for-the-badge"/>
  <img src="https://img.shields.io/github/license/MrRioja/OmniStack-9?color=blueviolet&logo=License&style=for-the-badge"/>
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/MrRioja/OmniStack-9?color=blueviolet&logo=JavaScript&logoColor=white&style=for-the-badge">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/MrRioja/OmniStack-9?color=blueviolet&style=for-the-badge">
</p>
<br>

<p align="center">
  <a href="#sobre">Sobre</a> •
  <a href="#tindev">Tindev</a> •
  <a href="#instalação">Instalação</a> •
  <a href="#tecnologias">Tecnologias</a> •
  <a href="#autor">Autor</a>  
</p>

<br><br><br>

## Sobre

<p>
  Projeto desenvolvido durante a <strong>Semana OmniStack 8</strong>, evento criado pela <strong><a href="https://rocketseat.com.br/">Rocketseat</a></strong>.   
  Um evento 100% online e GRATUITO, com conteúdo exclusivo e INÉDITO.

Ocorreu do dia 05 ao dia 11 de Agosto de 2019 e teve como intuito mostrar na prática o poder da stack
<strong><a href="https://nodejs.org/pt-br/">NodeJS</a></strong> +
<strong><a href="https://pt-br.reactjs.org/">ReactJS</a></strong> +
<strong><a href="https://reactnative.dev">React Native</a></strong> e como essas tecnologias podem te levar até os seus maiores objetivos como programador.

</p>

<br><br>

<img src="./readme/Wallpaper.png" alt="Logo" style="border-radius: 20px"/>

<br><br><br>

## Tindev

<p>
  O Tindev tem como objetivo unir programadores com interesses em comum para, quem sabe, construir projetos juntos ou até mesmo trocar experiências sobre esse mundo louco da programação...😅

A aplicação funciona como um Tinder, onde a pessoa se loga com o usuário do
<strong>
<a href="https://github.com/">Github</a>
</strong>
através dessa tela:

<br>
<img src="./readme/Login.png" alt="Login"/>
<br><br>

E logo após é direcionada para a tela principal onde estarão os cards dos outros usuários cadastrados na plataforma, conforme imagem abaixo:

<br>
<img src="./readme/Lista.png" alt="Lista"/>
<br><br>

Os cards contêm o nome e descrição dos Devs cadastrados, além dos botões de <strong>DISLIKE</strong> e <strong>LIKE</strong>.
Quando o Dev logado dá um like em um usuário da lista que deu like nele num outro momento, acontece o que é chamado de <strong>MATCH</strong>.

Esse evento é sinalizado para ambos os usuários em tempo real, utilizando Websocket. Assim que ocorre o match é apresentado na tela do usuário a seguinte tela:

<br>
<img src="./readme/Match.png" alt="Match"/>
<br><br>

Aqui temos uma demostração do evento de match desde o início. O usuário da esquerda da um like no usuário da direita, que momentos depois dá um like do Dev que curtiu o perfil dele e pronto...

<br><br>

<p align="center" ><img height="100" src="./readme/itsamatch.png" alt="It's a match" /></p>
<br><br>

<img src="./readme/Match.gif" alt="GIF Match"/>

</p>

<br><br><br>

## Instalação

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/).
Além disto é bom ter um editor para trabalhar com o código como [VSCode](https://code.visualstudio.com/)

### 🎲 Rodando o Back End (servidor)

```bash
# Clone este repositório
$ git clone git@github.com:MrRioja/OmniStack-9.git

# Acesse a pasta do projeto no terminal/cmd
$ cd OmniStack-9

# Vá para a pasta server
$ cd backend

# Instale as dependências
$ npm install
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn

# Execute a aplicação em modo de desenvolvimento
$ npm run dev
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn dev

# O servidor inciará na porta 3333 ou na porta definida no arquivo .env na variavel APP_PORT - acesse <http://localhost:3333>
```

### 🖥️ Rodando o Front End (Web)

```bash
# Clone este repositório
$ git clone git@github.com:MrRioja/OmniStack-9.git

# Acesse a pasta do projeto no terminal/cmd
$ cd OmniStack-9

# Vá para a pasta server
$ cd frontend

# Instale as dependências
$ npm install
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn

# Execute a aplicação em modo de desenvolvimento
$ npm run start
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn start

# O servidor inciará na porta 3000 - acesse <http://localhost:3000>
```

### 📱 Rodando o App (Mobile)

```bash
# Clone este repositório
$ git clone git@github.com:MrRioja/OmniStack-9.git

# Acesse a pasta do projeto no terminal/cmd
$ cd OmniStack-9

# Vá para a pasta server
$ cd mobile

# Instale as dependências
$ npm install
# Caso prefira usar o Yarn execute o comando abaixo
$ yarn

# Execute a aplicação
$ expo start

# Será aberto no terminal o menu do Expo onde poderá scanear o QR Code para executar o app diretamente no seu celular ou as opções de executar no emulador android ou iOS
```

## Tecnologias

<img align="left" src="https://profilinator.rishav.dev/skills-assets/nodejs-original-wordmark.svg" alt="Node.js" height="75" />

<img align="left" src="https://profilinator.rishav.dev/skills-assets/express-original-wordmark.svg" alt="Express.js" height="75"/>

<img align="left" src="https://profilinator.rishav.dev/skills-assets/react-original-wordmark.svg" alt="React" height="75" />

<br><br><br><br><br><br>


## Autor

<div align="center">
<img src="https://badges.pufler.dev/contributors/MrRioja/Omnistack-8?size=100&padding=5&bots=false"/>
<h1>Luiz Rioja</h1>
<strong>Backend Developer</strong>
<br/>
<br/>

<a href="https://linkedin.com/in/luizrioja" target="_blank">
<img alt="LinkedIn" src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://github.com/mrrioja" target="_blank">
<img alt="GitHub" src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="mailto:lulyrioja@gmail.com?subject=Fala%20Dev" target="_blank">
<img alt="Gmail" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

<a href="https://api.whatsapp.com/send?phone=5511933572652" target="_blank">
<img alt="WhatsApp" src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>

<a href="https://join.skype.com/invite/tvBbOq03j5Uu" target="_blank">
<img alt="Skype" src="https://img.shields.io/badge/SKYPE-%2300AFF0.svg?style=for-the-badge&logo=Skype&logoColor=white"/>
</a>

<br/>
<br/>
</div>
