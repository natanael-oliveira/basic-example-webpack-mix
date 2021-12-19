<p align="center">
    <img src="src/images/webpack-logo.png" width="100px">
</p>
<h1 align="center">Basic Example Webpack Mix</h1>
<br>


#### A propósta do Webpack Mix é facilitar a configuração do webpack fornecendo uma API limpa e eficiênte com suporte a vários pré-processadores CSS e Javascript comuns.


## Instalação

```JS
git clone https://github.com/natanael-oliveira/basic-example-webpack-mix
cd example-webpack-mix
npm install
```

## Executar projeto
```JS
npm hot // open browser localhost:8080
```
![index.html](/src/images/index.png)

## Estrutura do projeto
    |--dist/
    |--node_modules/
    |--src/
    |   |--images/
    |   |--js/ 
    |   |--scss/
    |--package.json
    |--webpack.mix.js
    


## Exemplo de configuração
#### webpack.mix.js

```JS
let mix = require('webpack-mix');

mix.js('src/js/app.js', 'dist/')
    .sass('src/scss/app.scss', 'dist/')
    .setPublicPath('dist');

```

## Dependências
#### package.json
```JSON
    "webpack-mix": "^3.0.0",

    /* resolve varáveis de ambiente */
    "cross-env": "^7.0.3",

    /* pré-processadores */
    "resolve-url-loader": "^3.1.0",
    "sass": "^1.45.0",
    "sass-loader": "^8.0.2",
    "vue-template-compiler": "^2.6.14",
```
## Scripts
#### package.json
```JSON
"scripts": {
    "dev": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/webpack-mix/setup/webpack.config.js",
    "watch": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --watch --progress --hide-modules --config=node_modules/webpack-mix/setup/webpack.config.js",
    "hot": "cross-env NODE_ENV=development webpack-dev-server --inline --hot --config=node_modules/webpack-mix/setup/webpack.config.js",
    "prod": "cross-env NODE_ENV=production node_modules/webpack/bin/webpack.js --progress --hide-modules --config=node_modules/webpack-mix/setup/webpack.config.js"
}
```
### Para mais detalhes sobre instalação e configuração do Webpack Mix consulte a documentação
[Consultar Documentação](https://github.com/devanandb/webpack-mix/tree/master/docs)