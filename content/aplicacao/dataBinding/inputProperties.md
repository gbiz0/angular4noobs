# Input Properties

Input properties no Angular é uma maneira de compartilhar informações do componente pai com o componente filho, permitindo que os componentes se comuniquem e exibam dados de maneira coordenada. Isso é fundamental para a construção de componentes reutilizáveis e para a criação de hierarquias de componentes interconectados.

**Vamos ao Exemplo agora**

Nesse exemplo vamos utilizar 2 componentes:

**data-binding (componente pai)** 

_data-bindin.component.ts_
```ts
import { Component } from '@angular/core';

@Component({
    selector: 'app-data-bindin',
    templateUrl: './data-bindin.component.html',
    styleUrls: ['./data-bindin.component.css'],
})
export class DataBindinComponent {}
```
_data-bindin.component.html_

```html
 <article>
      <h3>Input Properties</h3>

  </article>
```

**input-property (componente filho)**

_input-property.component.ts_
```ts
import { Component } from '@angular/core';

@Component({
    selector: 'app-curso',
    templateUrl: './input-property.component.html',
    styleUrls: ['./input-property.component.css'],
})
export class InputPropertyComponent {}
```

_input-property.component.html_
```html
<p>Input Properties</p>
```

**Continuando...**

O que queremos agora é passar uma informação do componente pai para o componente filho, vamos primeiro chamar o componente filho no componente pai, adicionando o selector do componente filho no componente pai:
```html
 <article>
      <h3>Input Properties</h3>

      <app-curso></app-curso>
  </article>
```

vamos dizer que queremos passar uma propriedade chamada **nomedoCurso** do componente pai para o componente filho:

```ts
import { Component } from '@angular/core';

@Component({
    selector: 'app-data-bindin',
    templateUrl: './data-bindin.component.html',
    styleUrls: ['./data-bindin.component.css'],
})
export class DataBindinComponent {
  
    nomeDoCurso: string = 'Angular';
}
```

Adicionamos a variavel no componente pai e agora vamos atualizar o template do componente pai fazendo um property binding na tag do selector:

```html
 <article>
      <h3>Input Properties</h3>

      <app-curso [nome]='nomeDoCurso'></app-curso>
  </article>
```

__Vale lembrar que você vai ter que colocar a variavel que está no componente filho para realizar o property binding recebendo a variavel que está no componente pai__

Agora vamos definir a variavel no componente filho para que o mesmo receba por Input Properties:

```ts
import { Component, Input } from '@angular/core';

@Component({
    selector: 'app-curso',
    templateUrl: './input-property.component.html',
    styleUrls: ['./input-property.component.css'],
})
export class InputPropertyComponent {
    @Input() nome = '';
}
```

Agora vamos atualizar o template para que quando o componente pai chame o componente filho o dado seja mostrado pelo componente filho:

```html
<p>{{ nome }}</p>
```

Dessa forma ao atualizar a pagina e quando o componente pai chamar o componente filho, virá o valor do componente pai dentro do componente filho:

<br><img align="center" src="/content/image/dataBinding/InputProperties/InputProperties.png" alt="Arquivos DataBinding"><br>