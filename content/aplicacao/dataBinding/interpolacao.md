# Interpolação

A interpolação representa a forma mais frequente de aplicar o binding, desempenhando a função de transmitir valores provenientes de propriedades e os resultados de métodos do componente para o template HTML. Nesse processo, o nome das propriedades ou dos métodos é inserido entre chaves duplas. A título de exemplo: **{{ Propriedade }}**

**Vamos agora ao exemplo:**

Desenvolvi um componente denominado "data-binding". A seguir, no nosso arquivo TypeScript, inseri a seguinte variável:

<br><img align="center" src="/content/image/dataBinding/dataBinding.png" alt="Arquivos DataBinding"><br>

Após esse passo, vou utilizar a técnica de interpolação para exibir as informações desta variável no meu template, como mostrado abaixo:

<br><img align="center" src="/content/image/dataBinding/dataBinding2.png" alt="Arquivos DataBinding"><br>

Desta maneira, ao executarmos nossa aplicação, iremos visualizar a informação da seguinte forma:

<br><img align="center" src="/content/image/dataBinding/dataBinding3.png" alt="Arquivos DataBinding"><br>

Além disso, é importante destacar que essa não é a única abordagem viável. Existem várias outras formas pelas quais podemos realizar a interpolação, como por exemplo, utilizando métodos, objetos, entre outros. Um exemplo concreto seria:

No nosso arquivo TypeScript, criamos um objeto e um método da seguinte maneira:
<br><img align="center" src="/content/image/dataBinding/dataBinding4.png" alt="Arquivos DataBinding"><br>

Em seguida, faremos a chamada desses elementos no nosso template:

<br><img align="center" src="/content/image/dataBinding/dataBinding5.png" alt="Arquivos DataBinding"><br>

Resultando na configuração a seguir:

<br><img align="center" src="/content/image/dataBinding/dataBinding6.png" alt="Arquivos DataBinding"><br>

