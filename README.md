# FICO Website

O site funciona com Hugo Server, utilizando o template [Tella](https://github.com/opera7133/tella) como submódulo no projeto em `themes\tella`

## Instalar

### Hugo

O Hugo depende de alguns pacotes:

````bash
sudo apt install -y nodejs
sudo apt install -y npm

# também é necessário instalar o Go
# Na doc, é exigido o Go versão 1.20, mas eu rodei com 1.13.8 sem problemas
sudo apt install -y golang
````

Deve-se utilizar o Hugo versão Extended na versão mais recente:

````bash
wget https://github.com/gohugoio/hugo/releases/download/v0.111.2/hugo_extended_0.111.2_linux-amd64.deb
apt install ./hugo_extended_0.111.2_linux-amd64.deb
````

## Inicialização

Após clonar o repo, é necessário iniciar os submódulos

````bash
cd fico-ita.github.io
git submodule update --init --recursive
````
e instalar os pacotes do node.js:

````bash
npm install
````

## Execução

Para compilar e servir a página.

````bash
hugo server -p 8888
````

Caso ocorrer algum problema, apague a pasta `public` antes de servir a página.

Para compilar use o comando abaixo. Será compilada a página para a pasta `public`.

````bash
hugo
````
