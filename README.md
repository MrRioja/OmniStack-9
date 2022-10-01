<p align="center">
  <img src="./frontend/src/assets/logo.svg" alt="Logo" width="300"/>
  <br/>
</p>

<h3 align="center">
Spots a um clique de distância.
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
  <a href="#aircnc">Aircnc</a> •
  <a href="#instalação">Instalação</a> •
  <a href="#tecnologias">Tecnologias</a> •
  <a href="#autor">Autor</a>  
</p>

<br><br><br>

## Sobre

<p>
  Projeto desenvolvido durante a <strong>Semana OmniStack 9</strong>, evento criado pela <strong><a href="https://rocketseat.com.br/">Rocketseat</a></strong>.   
  Um evento 100% online e GRATUITO, com conteúdo exclusivo e INÉDITO.

Ocorreu do dia 30 de Setembro ao dia 06 de Outubro de 2019 e teve como intuito mostrar na prática o poder da stack
<strong><a href="https://nodejs.org/pt-br/">NodeJS</a></strong> +
<strong><a href="https://pt-br.reactjs.org/">ReactJS</a></strong> +
<strong><a href="https://reactnative.dev">React Native</a></strong> e como essas tecnologias podem te levar até os seus maiores objetivos como programador.

</p>

<br/><br/>

<img src="./readme/Wallpaper.png" alt="Logo" style="border-radius: 20px"/>

<br/><br/><br/>

## Aircnc

A aplicação AirCnC tem como objetivo servir de vitrine para empresas que querem disponibilizar spots para profissionais realizarem seus trabalhos no local. Sendo uma especie de co-working, o aplicativo possui dois modos de acesso: aplicação web e mobile, cada qual com sua responsabilidade e funcionalidades especificas as quais serão descritas abaixo:

### AirCnC - Aplicação web

A responsabilidade da aplicação web do AirCnC é o cadastro dos spots. É uma página web disponibilizada para que as empresas criem seu cadastro e realize o cadastro dos spots que desejam disponibilizar para seus futuros visitantes.

O fluxo é bem simples, primeiro o responsável pela empresa realiza o login na aplicação com seu email através da página abaixo:

![Página de login - Web](./readme/Web%20Login%20Screen.png)

Após o login o usuário é direcionado para a página dashboard que exibirá os spots já cadastrados e a opção de cadastro de novos spots, conforme tela abaixo:

![Dashboard AirCnC - Web](./readme/Web%20Dashboard.png)

Como vemos na tela acima, além dos spots já cadastrados, temos um botão para realizar novos cadastros. O cadastro de spot é bem simples e os únicos dados necessários são:

- Imagem do spot.
- Nome da empresa.
- Tecnologias utilizadas pela empresa.
- Valor da diária do spot.

Abaixo um exemplo de cadastro de um spot:

![Página de cadastro de Spot AirCnC - Web](./readme/Web%20Spot's%20Form.png)

Com os spots disponibilizados para os demais usuários, basta aguardar que ocorra um agendamento e pronto, teremos a opção de aceitar ou rejeitar a solicitação de reserva que ocorre em tempo real com a comunicação entre mobile e web realizada através de websocket.

Abaixo um exemplo de alerta de solicitação de reserva na tela de dashboard. Pelo mobile, quando há a solicitação de reserva, o dono do spot é comunicado em tempo real (caso esteja com sessão ativa) sobre quem, quando e qual spot está sendo requisitado, conforme imagem abaixo:

![Alerta de solicitação de agendamento AirCnC - Web](./readme/Web%20Booking%20Alert.png)

### AirCnC - Aplicação mobile

A aplicação móvel tem como finalidade servir de ponte entre os spots disponíveis e os usuários que buscam spots para diárias. Ao se cadastrar na aplicação, o usuário informa seu email como forma de identificação e as tecnologias com que trabalha, dando a possibilidade para ele alocar um spot em uma empresa que utiliza a mesma stack dele para fortalecer o networking e a troca de conhecimento.

<img src="./readme/Mobile Login Screen.png" width="250"  />

Após o cadastro, o usuário irá para a tela de dashboard onde os spots serão exibidos separados por tecnologia, conforme imagem abaixo:

<img src="./readme/Mobile Dashboard.png" width="250"  />

Com o spot escolhido, basta o usuário clicar no botão de reserva e escolher a data que deseja visita-lo. Ao concluir o agendamento o dono do spot será alertado em tempo real que determinado usuário deseja alugar o spot na data preenchida pelo usuário. Seguem as telas desse fluxo:

|                    Formulário de agendamento                    |                  Confirmação de agendamento                   |
| :-------------------------------------------------------------: | :-----------------------------------------------------------: |
| <img src="./readme/Mobile Appointment Form.png" width="50%"  /> | <img src="./readme/Mobile Booking Finish.png" width="50%"  /> |

Após a solicitação ser enviada, ficará pendente a resposta do dono do spot. Quando a reserva for aceita ou rejeitada, o usuário que a solicitou será notificado com as informações da reserva e seu status, vide imagens a seguir:

|                         Reserva aceita                          |                        Reserva rejeitada                        |
| :-------------------------------------------------------------: | :-------------------------------------------------------------: |
| <img src="./readme/Mobile Booking Approved.png" width="50%"  /> | <img src="./readme/Mobile Booking Rejected.png" width="50%"  /> |

<br/><br/>

## Instalação

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/) e [Docker](https://www.docker.com/).
Além disto é bom ter um editor para trabalhar com o código como [VSCode](https://code.visualstudio.com/).

### Criando container do mongoDB localmente

O comando abaixo irá baixar a imagem docker do mongo e criar um container com as configurações e senhas abaixo. Caso queira executar o mongo de outra maneira basta alterar a string de conexão presente no arquivo [server](./backend/src/server.js).

```bash
docker container run --name omnistack9 -e MONGO_INITDB_ROOT_USERNAME=omnistack9 -e MONGO_INITDB_ROOT_PASSWORD=admin -p 27017:27017 -d -v "mongoVolume:/data/db" mongo
```

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

# O servidor inciará na porta 3333 ou na porta definida no arquivo .env na variável APP_PORT - acesse <http://localhost:3333>
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
<img src="https://images.weserv.nl/?url=avatars.githubusercontent.com/u/55336456?v=4&h=100&w=100&fit=cover&mask=circle&maxage=7d" />
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

<br/><br/>

</div>
