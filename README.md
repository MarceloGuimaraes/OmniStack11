  
![Be The Hero](https://github.com/MarceloGuimaraes/OmniStack11/blob/master/frontend/src/assets/logo.svg)

# Semana OmniStack 11.0 - [Rocketseat](https://rocketseat.com.br/) - 23/03/2020 à 27/03/2020
Resultado de uma semana onde foi desenvolvida uma aplicação chamada BE THE HERO. Onde ONGs Realizam cadastros de casos atraves da WEB ou MOBILE, solicitando ajuda. E por meio do aplicativo MOBO, é possivel contribuir nos casos ( ser o herói ). 
------------

## Stack Utilizada

### Front-End

 - [React](https://pt-br.reactjs.org/ "React")
Uma biblioteca interativa para criar interfaces com o usuário.

### Mobile

- [React Native](https://reactnative.dev/)
Com o lema: "Learn once, write anywhere", utiliza os mesmos conceitos do React para criar interfaces nativas para dispositivos móveis. Com um código e uma linguagem é possível criar apps para Android e iOS.

- [Expo](https://expo.io/)
É um framework e uma plataforma universal para aplicação React, definindo ferramentas construídas em React Native e plataformas nativas que ajudam o desenvolvedor a construír, lançar e interagir rapidamente no iOS e Android a partir do mesmo código JavaScript/TypeScript. 

### Back-End

- [NodeJs](https://nodejs.org/pt-br/)
Node.js® é um runtime JavaScript desenvolvido com o Chrome's V8 JavaScript engine. Basicamente.

- [SQLite](https://www.sqlite.org/index.html)
Este é o nosso banco de dados. Do tipo SQL, onde a estrutura é bem definida. 


------------


## O Projeto:

Uma aplicação para que ONG's possam divulgar seus casos e conseguir financiamento voluntário para cada um deles.

### 1º Dia

Foi apresentado o projeto, cujo mockup do layout foi construído no [figma](https://www.figma.com/). Também fizemos o ritual do "Hello World" em cada tecnologia utilizada. É possível acessar esses tutoriais aqui:

- [NodeJS](https://nodejs.org/en/docs/guides/getting-started-guide/)
- [React](https://reactjs.org/docs/hello-world.html)

### 2º Dia

No segundo dia construímos o back-end da aplicação com as seguintes tecnologias:

- [NodeJS](https://nodejs.org/en/docs/guides/getting-started-guide/)
Utilizamos o nodejs como base da aplicação para gerenciar a conexão entre o front-end e o banco de dados. Foram utilizadas as seguintes bibliotecas:

	 - [Express](https://expressjs.com/) => Utilizado para gerenciar as requisições, rotas e URLS. As configurações de conexão podem ser acessadas [aqui](https://github.com/MarceloGuimaraes/OmniStack11/blob/master/backend/src/routes.js) e [aqui](https://github.com/MarceloGuimaraes/OmniStack11/blob/master/backend/src/app.js)
	 - [Nodemon](https://nodemon.io/) => Utilzado para monitorar as alterações em todos os arquivo e dar "restart" no servidor.
	 - [SQLite](https://www.sqlite.org/index.html) => Para o banco de dados.
	 - [Knex](http://knexjs.org/) => Para gerenciar o banco de dados, com o CRUD completo. O banco de dados foi instalado através do Knex conforme mostrado [aqui](http://knexjs.org/#Installation).
	 - [CORS](https://expressjs.com/en/resources/middleware/cors.html) => Para permitir o acesso do front-end e mobile à aplicação. 

##### Definição de Entidades e Funcionalidades:

- Entidades:
	 - [ONG](https://github.com/MarceloGuimaraes/OmniStack11/blob/master/backend/src/database/migrations/20200324230752_create_ongs.js)
	 - [Caso (Incident)](https://github.com/MarceloGuimaraes/OmniStack11/blob/master/backend/src/database/migrations/20200324231501_create_incidents_.js)
- Funcionalidades
	 - Login/Logout da ONG
	 - Cadastro da ONG
	 - Deletar Casos
	 - Listar casos específicos de uma ONG
	 - Listar todos os casos
	 - Entrar em contato com a ONG

### 3º Dia

Nesse dia contruímos o front-end da aplicação, utilizando [React](https://reactjs.org/docs/hello-world.html) e outras bibliotecas:

- [Axios](https://github.com/axios/axios) => cliente HTTP, onde é possível fazer request HTTP do nodeJs.
- [React Icons](https://react-icons.netlify.com/#/icons/md) => biblioteca que permite a inserção de ícones como componentes dentro da aplicação.

### 4º Dia

Nesse dia construímos o app mobile, utilizando o [React Native](https://reactnative.dev/) e [Expo](https://expo.io/).

Utlizamos a [Stack Navigation](https://reactnavigation.org/docs/stack-navigator/) para o nosso app.

Outras bibliotecas utilizadas nesse projeto mobile:
- [expo-constants](https://docs.expo.io/versions/latest/sdk/constants/#constantsstatusbarheight) => Utilizado para estilizar o margin na parte de cima do smartphone para não ficar abaixo da barra de status.
- [expo-mail-composer](https://docs.expo.io/versions/latest/sdk/mail-composer/) => Utilizado para a funcionalidade de envio de email para a ONG.
- [deep-linking](https://reactnavigation.org/docs/deep-linking/) => Utilizado para acessar o What's app na funcionalidade de entrar em contato com a ONG.
- [INTL](https://github.com/andyearnshaw/Intl.js#readme) => Utilizado para formatar os números na UI.

### 5º Dia - Tópicos avançados

Nesse dia adicionamos validação e testes na nossa aplicação:

- [celebrate](https://www.npmjs.com/package/celebrate) => Utilizado para fazer as validações nos dados enviados ao banco de dados.
- [Joi](https://www.npmjs.com/package/joi) => Utilizado em conjunto com o celebrate para a validação dos dados.
- [Jest](https://jestjs.io/) => Utilizado para os testes unitários e de integração, implementados [aqui](https://github.com/MarceloGuimaraes/OmniStack11/tree/master/backend/tests)
- [cross-env](- [cross-env](https://github.com/kentcdodds/cross-env#readme) => Utilizado para utilizar variáveis de ambiente para os testes de integração.
- [supertest](https://github.com/visionmedia/supertest) => Utilizado para os testes com HTTP.


------------

### Instalação

Clone o repositório, utilizando **git clone** ou faça o **download** do repositório.
```sh
git clone https://github.com/MarceloGuimaraes/OmniStack11.git
cd OmniStack11
npm install
```
----

Após clonar ou baixar o repositório instale as dependências necessárias:

Utilize o **npm** para instalar as dependências nas pastas *backend*, *frontend* e *mobile*.

```
npm install
```
Após instalar as dependências você precisa rodar o comando do knex para criar o banco de dados SQLite e as rodar as migrações. 

```
npx knex migrate:latest
```

Após a geração do banco de dados é hora de executar...

### Execução

**Clonando o projeto** 
```sh
git clone https://github.com/MarceloGuimaraes/OmniStack11.git
cd semana-omnistack-11
npm install
```
**Iniciando Backend** 
```sh
cd backend
npm start
```
**Iniciando Frontend** 
```
cd frontend
npm start
```
**Iniciando mobile** 
```
cd mobile
npm start
```
   **ou**
```
cd mobile
expo start
```

Para visualização da aplicação mobile utilize o celular com o aplicativo *Expo* ou emulador Android/iOS.