# Two Way Data Binding

Ao contrário do Angular JS, no Angular, foram introduzidas várias otimizações de desempenho no binding bidirecional. Devido a essas melhorias, o binding bidirecional tradicional não está mais presente. Em vez disso, temos uma combinação do binding de atributos e do binding de eventos. Quando se trata de atualizar tanto o template quanto o componente, entra em cena a diretiva ngModel. Essa diretiva é empregada nos elementos de um formulário e simplifica consideravelmente a aplicação do binding bidirecional.

Nesse tipo de binding, como já mencionei, a combinação dos dois tipos de binding é expressa por uma sintaxe chamada **"banana in the box"** ou **[(ngModel)]**. Essa sintaxe realmente faz lembrar duas bananas, que representam os parênteses **"()"**. A caixa é uma representação dos colchetes **"[]"**. Uma maneira simples de fixar essa sintaxe é visualizar a seguinte figura:

<br><img align="center" src="/content/image/dataBinding/dataBinding12.png" alt="Arquivos DataBinding"><br>

Conforme vocês podem perceber, estou empregando o ngModel e utilizando interpolação para ilustrar o seu funcionamento. Um valor foi atribuído a uma variável chamada "nome" no arquivo TypeScript, como apresentado abaixo:


<br><img align="center" src="/content/image/dataBinding/dataBinding13.png" alt="Arquivos DataBinding"><br>

Ao efetuar uma modificação no campo de entrada, essa alteração é automaticamente refletida na interpolação. Isso ocorre porque a alteração feita no template é equivalente à alteração realizada no componente:

<br><img align="center" src="/content/image/dataBinding/dataBinding14.gif" alt="Arquivos DataBinding"><br>

A seguir, realizarei uma alteração utilizando somente o modelo (model) e vocês perceberão que essa alteração afeta apenas o template por meio do campo de entrada (input), não tendo impacto no componente em si.

Alteramos o input para receber um propertyBinding

<br><img align="center" src="/content/image/dataBinding/dataBinding15.png" alt="Arquivos DataBinding"><br>
 
Com o gif abaixo vocês podem perceber que a alteração é apenas no template e não é realizado no componente:

<br><img align="center" src="/content/image/dataBinding/dataBinding16.gif" alt="Arquivos DataBinding"><br>