# Output Properties

No Angular, "Output Properties" se referem a mecanismos que permitem que um componente filho notifique ou emita eventos para o componente pai. Essas propriedades de saída, conhecidas como "event emitters", possibilitam que um componente filho informe o componente pai sobre ações ou ocorrências relevantes. Esse recurso aprimora a interação entre componentes, permitindo que o componente pai responda a eventos gerados pelo componente filho.

**Exemplo Prático**

Para ilustrar o conceito, consideremos um cenário com dois componentes:

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
      <h3>Output Properties</h3>

      <contador></contador>
  </article>

```

**output-property (componente filho)**

_output-property.component.ts_
```ts
import { Component } from '@angular/core';

@Component({
    selector: 'contador',
    templateUrl: './output-property.component.html',
    styleUrls: ['./output-property.component.css'],
})
export class OutputPropertyComponent {
   
}
```

_input-property.component.html_
```html
<div>
</div>
```

**Desenvolvendo o Exemplo**

Nós iremos trabalhar dentro do Output-property, vamos criar dois buttons um de adição e outro de subtração e no meio deles vamos adicionar um input com o atributo _readonly_ e com um valor inicial utilizando property binding:

_output-property.component.html_
```html
<div>
  <button class='btn btn-primary'>+</button>
  <input type='text' [value]='valor' readonly>
  <button class='btn btn-primary'>-</button>
</div>
```
_output-property.component.ts_
```ts
import { Component } from '@angular/core';

@Component({
    selector: 'contador',
    templateUrl: './output-property.component.html',
    styleUrls: ['./output-property.component.css'],
})
export class OutputPropertyComponent {
    valor = 0;
}
```

Com isso nós temos o seguinte resultado atualmente:

<br><img align="center" src="/content/image/dataBinding/outputProperties/outPutProperties.png" alt="Arquivos DataBinding"><br>

Agora vamos utilizar o event Binding para escutar o evento de click nos botões e realizar alguma ação neles:

_output-property.component.html_
```html
<div>
  <button class='btn btn-primary' (click)="incrementa()">+</button>
  <input type='text' [value]='valor' readonly>
  <button class='btn btn-primary' (click)="decrementa()">-</button>
</div>
```
_output-property.component.ts_
```ts
import { Component } from '@angular/core';

@Component({
    selector: 'contador',
    templateUrl: './output-property.component.html',
    styleUrls: ['./output-property.component.css'],
})
export class OutputPropertyComponent {
    valor = 0;

    incrementa() {
        this.valor++;
    }

    decrementa() {
        this.valor--;
    }
}

```

Com a adição desses métodos agora ao apertar o botão + ele irá aumentar o valor e apertar o - ele irá diminuir o valor, agora vamos expor esse valor para que o dataBindin consiga passar um valor para esse valor também:

_output-property.component.ts_
```ts
import { Component, Input } from '@angular/core';

@Component({
    selector: 'contador',
    templateUrl: './output-property.component.html',
    styleUrls: ['./output-property.component.css'],
})
export class OutputPropertyComponent {
    @Input() valor = 0;

    incrementa() {
        this.valor++;
    }

    decrementa() {
        this.valor--;
    }
}
```

_data-bindin.component.html_
```html
 <article>
      <h3>Output Properties</h3>

      <contador [valor]='10'></contador>
  </article>
```

Agora o valor está sendo passado pelo **InputProperties**, mas como estamos falando de **OutPutProperties**, vamos fazer o seguinte, vamos expor o evento mudou toda vez que clicar no botão de mais ou de menos, e vamos fazer o componente pai escutar o valor e saber quando ele foi alterado para que ele possa realizar alguma ação. Vejamos:

Vamos fazer as primeiras alterações nos componentes:

No componente filho, vamos fazer a seguinte alteração, vamos atribuir uma variavel do tipo EventEmitter para que ele emita o evento e vamos atribuir a essa variavel a anotação *@Output*, conforme o codigo abaixo:

_output-property.component.ts_
```ts
import { Component, EventEmitter, Input, Output } from '@angular/core';

@Component({
    selector: 'contador',
    templateUrl: './output-property.component.html',
    styleUrls: ['./output-property.component.css'],
})
export class OutputPropertyComponent {
    @Input() valor = 0;
    @Output() mudouValor = new EventEmitter();

    incrementa() {
        this.valor++;
        this.mudouValor.emit({ novoValor: this.valor });
    }

    decrementa() {
        this.valor--;
        this.mudouValor.emit({ novoValor: this.valor });
    }
}
```

Já no componente pai, vamos atribuir um event binding nele chamando um método e passando o evento por ele:

_data-bindin.component.html_
```html
  <article>
      <h3>Output Properties</h3>

      <contador [valor]='valorInicial' (mudouValor)='onMudouvalor($event)'></contador>
  </article>
```

e por ultimo, vamos verificar se está sendo passado o evento para o componente pai utilizando o console log nesse método:

_data-bindin.component.ts_
```ts
  import { Component } from '@angular/core';

@Component({
    selector: 'app-data-bindin',
    templateUrl: './data-bindin.component.html',
    styleUrls: ['./data-bindin.component.css'],
})
export class DataBindinComponent {
    nomeDoCurso: string = 'Angular';
    valorInicial = 10;

    onMudouvalor(evento: any) {
        console.log(evento);
    }
}
```

Dessa forma, após ter alguma alteração ou algum clique no botão, o componente pai vai está recebendo essa informação do componente filho:


<br><img align="center" src="/content/image/dataBinding/OutputProperties/OutputProperties2.png" alt="Arquivos DataBinding"><br>



