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

```
node -v
npm -v
```

Depois, execute o seguinte comando para instalar a Angular CLI:

```
npm install @angular/cli
```

### macOS
Caso você esteja utilizando o sistema da maçã, teremos que instalar o Node e o npm. Aqui também iremos instalar diretamente no <a href="https://nodejs.org/en/download">site oficial</a>. Para fazer uma instalação com segurança e sem erros, é recomendável baixar a versão LTS e, depois, seguir o assistente de instalação.

Após a instalação ser concluida, para garantir que o Node e o npm estejam instalados corretamente no macOS, vamos abrir o terminal e inserir os comandos abaixo, e o retorno deve ser a versão instalada na máquina.

```
node -v
npm -v
```

Depois, execute o seguinte comando para instalar a Angular CLI:

```
sudo npm install -g @angular/cli
```

### Debian/Ubuntu e derivados
Tá no Linux? Fica suave, para rodar nosso Angular aqui devemos instalar o Node, para isso siga os seguintes passos no seu terminal.

Primeiro, recarregue seu índice de pacotes local digitando:

```
sudo apt update
```

Em seguida, instale o Node.js:

```
sudo apt install nodejs
```

Verifique se a instalação ocorreu bem consultando o node pelo número de versão dele:

```
nodejs -v
```

Agora faça isso para instalar o pacote npm com o apt:

```
sudo apt install npm
```

Para garantir, atualize a versão npm para a versão mais recente executando o seguinte comando:

```
npm install  -g
```

Agora finalmente podemos instalar o Angular usando o npm conforme mostrado abaixo:

```
npm install -g @angular/cli
```

Depois de instalado, verifique a versão instalada do Angular usando o seguinte comando:

```
ng version
```

---

Que isso em fera, o Angular já está instalado corretamente? É hora de termos o nosso primeiro contato com a ferramenta!

<p align="right">
  <a href="https://github.com/gbiz0/angular4noobs/blob/main/content/intro/helloworld.md">Próximo -> Rodando uma página Angular</a>
</p>

<p align="left">
  <a href="https://github.com/gbiz0/angular4noobs#roadmap">Voltar para o menu principal</a>
</p>
