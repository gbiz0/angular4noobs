# Instalação

Bom, você agora está de fato mais próximo de criar seu primeiro projeto Angular, partiu para as instruções! 

## Sistemas Operacionais
- [Windows](https://github.com/gbiz0/angular4noobs/blob/main/content/intro/instalacao.md#windows)
- [macOS](https://github.com/gbiz0/angular4noobs/blob/main/content/intro/instalacao.md#macos)
- [Debian/Ubuntu e derivados](https://github.com/gbiz0/angular4noobs/blob/main/content/intro/instalacao.md#debianubuntu-e-derivados)

Algum problema com a instalação? Sem problemas colega! Clique <a href="https://angular.io/guide/setup-local">aqui</a> para acessar a documentação oficial de instalação!

### Windows
Primeiro, você precisa ter o Node e o npm instalados na sua máquina. Para facilitar vamos instalar diretamente no <a href="https://nodejs.org/en/download">site oficial</a> e baixar os arquivos binários para o Windows e, depois, seguir o assistente de instalação.

Para garantir que o Node e o npm estejam instalados em seu sistema Windows, vamos executar o comando abaixo em um prompt de comando, e o retorno deve ser a versão instalada na máquina.

``` bash
node -v
npm -v
```

Depois, execute o seguinte comando para instalar a Angular CLI:

``` bash
npm install @angular/cli
```

### macOS
Caso você esteja utilizando o sistema da maçã, teremos que instalar o Node e o npm. Aqui também iremos instalar diretamente no <a href="https://nodejs.org/en/download">site oficial</a>. Para fazer uma instalação com segurança e sem erros, é recomendável baixar a versão LTS e, depois, seguir o assistente de instalação.

Após a instalação ser concluida, para garantir que o Node e o npm estejam instalados corretamente no macOS, vamos abrir o terminal e inserir os comandos abaixo, e o retorno deve ser a versão instalada na máquina.

``` bash
node -v
npm -v
```

Depois, execute o seguinte comando para instalar a Angular CLI:

``` bash
sudo npm install -g @angular/cli
```

### Debian/Ubuntu e derivados
Tá no Linux? Fica suave, para rodar nosso Angular aqui devemos instalar o Node, para isso siga os seguintes passos no seu terminal.

Primeiro, recarregue seu índice de pacotes local digitando:

``` bash
sudo apt update
```

Em seguida, instale o Node.js:

``` bash
curl -fsSL https://deb.nodesource.com/setup_19.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
```

Agora faça isso para instalar o pacote npm com o apt:

``` bash
sudo apt install npm
```

Agora finalmente podemos instalar o Angular conforme mostrado abaixo:

``` bash
sudo npm install -g @angular/cli
```

Depois de instalado, verifique a versão instalada do Angular usando o seguinte comando:

``` bash
ng version
```

Caso seja mostrado uma mensagem do tipo:
```
Node.js version v12.22.9 detected.
The Angular CLI requires a minimum Node.js version of either v14.20, v16.14 or v18.10.

Please update your Node.js version or visit https://nodejs.org/ for additional instructions.
```

Basta instalar uma versão mais recente do seu NVM, usando o comando a seguir:
```bash
nvm install 18
```
---

Que isso em fera, o Angular já está instalado corretamente? É hora de criarmos nosso primeiro projeto Angular!

<p align="right">
  <a href="https://github.com/gbiz0/angular4noobs/blob/main/content/intro/helloworld.md">Próximo -> Rodando uma página Angular</a>
</p>

<p align="left">
  <a href="https://github.com/gbiz0/angular4noobs#roadmap">Voltar para o menu principal</a>
</p>
