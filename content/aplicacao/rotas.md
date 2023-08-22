# Rotas

## Como funciona as rotas no Angular?
As rotas no Angular permitem criar uma navegação fluida e organizada em aplicações de página única (Single Page Applications - SPAs). O sistema de roteamento facilita a exibição de diferentes componentes e visualizações com base nas URLs e nas ações do usuário. São extremamente fundamentais para criar aplicações web interativas e navegáveis. Elas permitem a exibição dinâmica de conteúdo com base nas URLs e nas ações do usuário, proporcionando uma experiência de usuário rica e coesa.

## Como criar rotas no seu projeto?
Primeiramente vamos procurar nosso arquivo _app-routing.module.ts_, se não foi criado automaticamente podemos fazer isso manualmente, e vamos começar a editar como mostra o exemplo a seguir:
```ts
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { LoginComponent } from './login/login.component';
import { PagenotfoundComponent } from './pagenotfound/pagenotfound.component';


const routes: Routes = [
    {path: '', component: HomeComponent},
    {path: 'login', component: LoginComponent},
    {path: '**', component: PagenotfoundComponent}// para qualquer rota não encontrada
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

Depois disso, vamos para o template que gostariamos de exibir os componentes associados a rotas e adicionamos o nosso comando 'router'. 
```html
<div>
  <router-outlet></router-outlet>
</div>
```

---
Bom, aqui terminamos nosso último tópico de estudo básico do framework Angular!
<p align="right">
  <a href="https://github.com/gbiz0/angular4noobs/blob/main/content/aplicacao/rotas.md">Próximo -> Rotas</a>
</p>

<p align="left">
  <a href="https://github.com/gbiz0/angular4noobs#roadmap">Voltar para o menu principal</a>
</p>
