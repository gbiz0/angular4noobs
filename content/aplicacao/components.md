# Manipulação de Components

## O que são components?
No vasto mundo do Angular, os components são a base de tudo. Eles são os responsáveis por criar a interface do usuário, ou seja, o que o usuário vê e interage. Eles são formados por arquivos de template, de estilo e de classe. O template é o arquivo HTML, o estilo é o arquivo CSS e a classe é o arquivo TS (TypeScript), como é mostrado na imagem abaixo:

<br><img align="center" src="/content/image/componets.png" alt="Arquivos components"><br>

## Função de cada component
### app.component.html (Template)
O template é o arquivo HTML do component, ele é responsável por criar a interface do usuário, ou seja, o que o usuário vê e interage. Ele é formado por tags HTML e por diretivas, que são atributos que modificam o comportamento de uma tag HTML. Um exemplo de diretiva é o ngFor, que é responsável por criar uma lista de elementos. O template também pode conter interpolação, que é a forma de mostrar uma variável do arquivo TS no template. A interpolação é feita com o uso de chaves duplas, como é mostrado no exemplo abaixo:

```html
<h1>Olá, {{nome}}</h1>
```

### app.component.css (Style)
O style é o arquivo CSS do component, ele é responsável por estilizar o template. Ele é formado por seletores CSS e por propriedades CSS. Um exemplo de seletor é o seletor de classe, que é representado por um ponto, como é mostrado no exemplo abaixo:

```css
.nome-da-classe {
    color: red;
}
```

### app.component.ts (Class)
A classe é o arquivo TS do component, ele é responsável por controlar o template. Ele é formado por variáveis e por funções. Um exemplo de variável é a variável nome, que é representada por um tipo e um nome, como é mostrado no exemplo abaixo:

```ts
nome: string;
```

Um exemplo de função é a função ngOnInit, que é executada quando o component é inicializado, como é mostrado no exemplo abaixo:

```ts
ngOnInit() {
    this.nome = 'Gustavo';
}
```

### app.module.ts (Module)
O module é o arquivo TS do módulo, ele é responsável por importar e declarar os components. Ele é formado por imports e por declarations. Um exemplo de import é o import do BrowserModule, que é responsável por importar o módulo de funcionalidades do Angular, como é mostrado no exemplo abaixo:

```ts
import { BrowserModule } from '@angular/platform-browser';
```

Um exemplo de declaration é o declaration do AppComponent, que é responsável por declarar o component, como é mostrado no exemplo abaixo:

```ts
declarations: [
    AppComponent
]
```

### app-routing.module.ts (Routing)
O routing é o arquivo TS do roteamento, ele é responsável por criar as rotas do projeto. Ele é formado por imports e por declarations. Um exemplo de import é o import do RouterModule, que é responsável por importar o módulo de rotas do Angular, como é mostrado no exemplo abaixo:

```ts
import { RouterModule, Routes } from '@angular/router';
```

Um exemplo de rota é a rota de login, que é representada por um path e um component, como é mostrado no exemplo abaixo:

```ts
const routes: Routes = [
    {path: '', component: HomeComponent},
    {path: 'login', component: LoginComponent},
    {path: '**', component: PagenotfoundComponent}// para qualquer rota não encontrada
];
```

## Criando um component
Para criar um component, é necessário executar o comando abaixo:

```bash
ng generate component nome-do-component
```

O comando acima irá criar os arquivos HTML, CSS e TS do component, além de declarar o component no módulo. Para declarar o component no módulo, é necessário executar o comando abaixo:

```bash
ng generate component nome-do-component --module=nome-do-modulo
```

---

Já entendeu a importância dos components? Espero que sim! Agora vamos para o próximo tópico, que é sobre os templates do projeto.
<p align="right">
  <a href="https://github.com/gbiz0/angular4noobs/blob/main/content/aplicacao/template.md">Próximo -> Templates</a>
</p>

<p align="left">
  <a href="https://github.com/gbiz0/angular4noobs#roadmap">Voltar para o menu principal</a>
</p>


