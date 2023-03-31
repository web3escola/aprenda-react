# Utilizando o React

O React é composto por duas bibliotecas, que precisam ser utilizadas em conjunto no navegador, porém têm propósitos diferentes. A primeira biblioteca, React, faz o gerenciamento do DOM virtual. A segunda biblioteca, ReactDOM, faz a renderização do DOM; ou seja, transforma o DOM virtual no DOM real.

ReactDOM é utilizada apenas em navegadores. Podemos utilizar React também em mobile e desktop, através de **React Native** e **Eclipse**. Nesse caso, outra biblitoca irá fazer a renderização do DOM virtual, própria para o ambiente em questão. Neste livro não estudaremos esses casos.

Em princípio, para utilizar React em uma aplicação, basta incluir essas duas bibliotecas em nosso arquivo. A forma mais simples de fazer isso é conseguir esses arquivos em uma **CDN** (**C**ontent **D**elivery **N**etwork, ou Rede de Distribuição de Conteúdo). Essa não é a forma recomendada de utilizar React, porém vamos fazer isso aqui por uma questão didática. Para que fique claro que React é apenas uma biblioteca JavaScript; apenas um arquivo JavaScript.

O site oficial do React é [react.dev](https://react.dev). Não é mais possível encontrar links para as bibliotecas React diretamente no site (era possível no site antigo), porém basta procurar por React CDN no google. Abaixo, vou colocar o endereço para as duas bibliotecas, porém atente para o fato de que endereços na web são mutáveis. Caso os links abaixo não estejam mais funcionando, você deve procurar os links atuais em algum mecanismo de busca.


[https://unpkg.com/react@18/umd/react.development.js](https://unpkg.com/react@18/umd/react.development.js)

[https://unpkg.com/react-dom@18/umd/react-dom.development.js](https://unpkg.com/react-dom@18/umd/react-dom.development.js)

As bibliotecas acima são para desenvolvimento e não devem ser utilizadas em produção. Para produção, no entanto, iremos utilizar outros métodos de criar aplicações React, usando ferramentas como **vite**.

Para deixar o código limpo, vou escrever o mínimo possível de *tags*. Eu espero que seu conhecimento de HTML seja suficiente para preencher qualquer lacuna necessária.

```html
<html lang="en">
<head>
    <script src="https://unpkg.com/react@18/umd/react.development.js">
    </script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js">
    </script>
    <title>Document</title>
</head>
<body>
    <div id="root"></div>
</body>
</html>
```

A listagem acima é uma página HTML simples, incluindo os scripts necessários e com apenas um `div` cuja `id` é `root`. Veremos que tal *div* será a porta de entrada onde o React irá incluir o DOM.