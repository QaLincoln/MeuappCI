# MeuApp

**MeuApp** é uma aplicação web construída com **Angular**. O objetivo deste projeto é fornecer uma base sólida para o desenvolvimento de aplicações SPA (Single Page Application).

## Tecnologias utilizadas

- Angular
- TypeScript
- HTML/CSS
- RxJS
- Angular Router

## Pré-requisitos

Antes de começar, você precisará ter o seguinte instalado na sua máquina:

- [Node.js](https://nodejs.org/) (versão 16 ou superior)
- [Angular CLI](https://angular.io/cli) (instalado globalmente via npm)

## Como rodar o projeto localmente

1. Clone o repositório:

```bash
git clone https://github.com/nomegit/MeuappCI.git

rodar:

npm install   "instala as dependencias"  
npm run test  "roda os teste unitarios"

## 
2. instalar:

    1- java 17
    2-Instalar Jenkins
    3-Instala angula pelo terminal

3. configurar projeto:
Projeto criar:
    1- ng new MeuApp (para criar projeto em /angular);
    2- No package-json excluir Karma e instalar Jest;
    3-Excluir package-look-json e node modules;
    4-instalat jest: npm install --save-dev jest @types/jest ts-jest jest-preset-angular
    5-instalar npm i (instalar as dependências)

4. configura jest para rodar:
    1- Criar pasta jest.config.js
    2- Em SRC cria o arquivo setup-jest.js
    3- No arquivo angular.json apagar o segundo test e inserir esse:
    "test": {
          "builder": "@angular-builders/jest:run",
          "options": {
              "tsConfig": "tsconfig.spec.json",
              "stupeFile": "src/setup-jest.ts",
              "jestConfig": "jest.config.js"
            
          }
        }
    4- Em package.json deixar "test": "jest"
    5- Em ts.config inserir "esModuleInterop": true

5. Abrir Jenkins http://localhost:5000/   "Jenkins roda em ambiente local"
    1- file:///C:/ProgramData/Jenkins/.jenkins/secrets/initialAdminPassword  para pegar a senha
    2- senha: Inserir senha criada
    3- instalar node no Jenkins > Gerenciar Jenkins > plugins e tools


6. Ngrok (serve para comunicar webhook dispara para jeskins que foi feito o commit no GitHub ai ele roda a  pipeline)
    

    rodando no termina:
    1- rodar o token: ngrok config add-authtoken "inserir token"
    2- abrir o terminal na pasta ngrok e rodar .\ngrok.exe http 5000
    3- abrir a porta no chrome

7. Criar token no GitHub para jenkins tenha acesso:
    1- serttings > Developer settings > Personal access tokens(classics) e seta repôs e gerar token 
    2- No jenkis > gerenciar Jenkins > system e configura token e o nome da pipeline é 'meuapp_ci'
    3- No projeto visual studio cria a pasta jenkinsfile
    4- No Jenkins em nova tarefa configurar a pipeline
    5- No GitHub em settings webhooks e o link é o Jenkins caminho do nrok do terminal;


