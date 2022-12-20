# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.


### Estilizando com Sass:
Primeiramente, instalaremos o Sass, que é o pré-processador CSS que iremos utilizar no curso.
Colaremos o comando npm install --save-dev sass e executaremos com a tecla "Enter" para instalarmos.
De volta ao VSCode, acessaremos a pasta "pages" e dentro criaremos um novo documento chamado style.scss, e esta extensão .scss significa que se trata de um arquivo sass.


### Usando CSS Modules
Então, para conseguirmos criar uma classe única mesmo que o nome seja genérico para não termos o problema de sobreposição. Temos um pacote que o resolve, chamado CSS Modules.
Na parte "Installation", vemos a forma de instalá-lo com npm install -D typescript-plugin-css-modules

Então copiaremos apenas a linha com o nome de "plugins": fornecido no site, sem copiar também o "compilerOptions":, pois já temos o em nosso arquivo.

{
  "compilerOptions": {
    "plugins": [{ "name": "typescript-plugin-css-modules" }]
  }
}

A segunda mudança é, ao invés de só importarmos o .scss de uma só vez, o importaremos como se fosse um objeto. Então, no topo do código, faremos import style a partir de './style,module.scss'.

Copiaremos este style e, ao invés do className ser uma string, passará a ser uma variável JavaScript com uso das chaves. Dentro, colocaremos style.AppStyle para exportarmos um grande objeto no lugar de simplesmente aceitar strings como estilo, afinal já é um módulo.

import React from 'react';
import Formulario from '../components/Formulario';
import Lista from '../components/Lista';
import style from './style.module.scss';

function App() {
    return (
        <div className={style.AppStyle}>
            <Formulario />
            <Lista />
        </div>
    );
}

export default App;