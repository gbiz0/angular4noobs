# Services 

## O que são services dentro do Angular?

Em Angular, os serviços desempenham um papel crucial na organização e compartilhamento de funcionalidades, lógica de negócios e dados entre diferentes componentes da aplicação. Eles são classes TypeScript injetáveis que oferecem uma maneira eficaz de centralizar operações comuns e reutilizáveis.
São usadas principalmente para:
- Acesso de dados (Consumo de API)
- Gerenciamento de Estado
- Notificações e mensagens
- Autenticação e autorização

## Como criar services no seu projeto?

Primeiramente deve abrir o terminal e digitar o comando escrito a seguir:
```bash
ng generate service nome-do-servico
```

Depois você já pode implementar a função que quiser, deixei um exemplo abaixo apenas para fixar o conceito:
```ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class He4rtService {

  membros: any[] = [];
  constructor() { }
  adicionarMembros(novoMembros: any) {
    this.membros.push(novoMembros);
  }

  obterMembros() {
    return this.membros;
  }
}
```

E por último, basta apenas injetar o serviço em qualquer componente:
```ts
import { Component } from '@angular/core';
import { He4rtService } from './he4rt.service';

@Component({
  // ...
})
export class MeuComponente {

  constructor(private he4rtService: He4rtService) { }

  // Agora você pode usar os métodos do serviço dentro deste componente

}
```

---
Agora que você já pegou os temas vamos falar sobre nosso último tópico, as rotas!
<p align="right">
  <a href="https://github.com/gbiz0/angular4noobs/blob/main/content/aplicacao/rotas.md">Próximo -> Rotas</a>
</p>

<p align="left">
  <a href="https://github.com/gbiz0/angular4noobs#roadmap">Voltar para o menu principal</a>
</p>





