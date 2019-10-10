# Eslint + Prettier-para-VS-code
Como configurar Eslint junto a Prettier para visual estudio code 

<h1>que es Eslint?</h1>
es una herramienta cuya funcion es analizar nuesto codigo apartir de regas predefinias como estandar o buenas pacticas segun 
la comunidad, donde esta reglas las podesmos extender o modificar a nuesto gusto y poder mantener un codigo mas limpio. 

<h1>que es Prettier?</h1>
Prettier es un formateador de código para mejorar identacion y matener un codigo mas legible 

<h1>Como configurar </h1>

requisitos tener instalado 
-VS Code 
-Node js
-NPM o Yarn  

<h3>nota si no tienes yarn intalado sustituye por npm en los comandos</h3>

1- instlar Eslint en nuesto proyecto de js o instlar la extencion de VS Code

-- yarn add Eslint -D

-- https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

2- instlar prettier junto a la extencion de VS Code 

-- yarn add prettier -D

-- https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode

3- abrir una terminardentro del proyecto y ejecutar el siguiente comando si se instalo eslint en el royecto 
  
  ./node_modules/.bin/eslint --init

-- si se intalo la extencion entrar a la paleta de comando y escribir "create eslint configuration"

selecionar lo siguiente 
-- To check syntax, find problems, and enforce code style 
selecionar el tipo de impotacion yo utiliso 
  -- None of these
  
selecionar el framework que estar usando 
--muestra React y vue y nunguno de estos 

indicar si se usa typescript 
-- si o no

-- Marcar node y browser

selecionar la guia de estilo

-- Use a popular style guide

selecionar la configuracion se puede elegir entr las siguientes 3
Airbnb (https://github.com/airbnb/javascript) 
Standard (https://github.com/standard/standard) 
Google (https://github.com/google/eslint-config-google) 

yo utiliso Airbnb

selecionar el tipo de archivo de configuracion yo utiliso json

se intlaran dependecias nesesarias y generara el archivo .eslintrc

4- buscar las siguientes linas en archivo .eslintrc y cambiarlas 

 "extends": ["airbnb", "prettier"],
 
  "plugins": ["react", "prettier"],
  
  "rules": {
    "prettier/prettier": ["error"],
        "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx"] }],
        // aca dentro puede modificar las reglas segun la documentacion de Eslint
    }

5- instlar las siguientes depencias 

yarn add eslint-plugin-prettier eslint-config-prettier -D

6- activar guardado automatico, formato al pegar, fromato al guardar en vs code en los ajustes 

listo. 


