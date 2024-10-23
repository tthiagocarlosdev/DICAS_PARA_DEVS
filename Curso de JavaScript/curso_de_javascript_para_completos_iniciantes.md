# Curso de JavaScript

Professor: Felipe Rocha

[Aulas](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz)

## #01 - Introdução

### [00:00](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=0s) - Introdução 

### [00:48](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=48s) - Requisitos para você fazer este curso 

- HTML E CSS
- Vontade de aprender

### [01:33](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=93s) - O que é o JavaScript? 

- Linguagem de programação **interpretada**;
- Evolui conforme a especificação ***ECMAScript***;
- É executada no **navegador (cliente)** e também no **servidor (Node.js)**.



### [03:33](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=213s) - Por que aprender JavaScript? 

- É uma linguagem de programação **padrão** de **todos os navegadores**;
- Frameworks poderosíssimos, como **React**, utilizam JavaScript;
- Usado para desenvolver aplicações **full stack** (front-end e back-end);
- Usado para desenvolvimento **mobile** (React Native);
- Usado em aplicações  **desktop** (Electron);
- Basicamente, ele está por toda a parte.



### [05:04](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=304s) - O que você vai aprender neste curso 

- Variáveis e Tipos de Dados;
- Listas (arrays);
- Objetos;
- JSON;
- Loops(for, for of, while, forEach);
- Condicionais (if, else, switch, ternary);
- Funções e Arrow Functions;
- Programação Orientada a Objetos;
- Selecionar elementos do DOM;
- Manipular elementos do DOM;
- Eventos;
- Criar e validar um formulário.



### [05:48](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=348s) - Configuração do ambiente de desenvolvimento 

- VSCode;
- Dracula Theme;
- Prettier - Code formatter;
- Live Server.



### [07:54](https://www.youtube.com/watch?v=g08WcKOHeK0&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=1&t=474s) - Criando nosso primeiro arquivo JavaScript

- Criar um arquivo ***index.html***

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Curso de JavaScript</title>
</head>
<body>
    
</body>
</html>
```



- Criar um arquivo ***main.js***
- Importar o **main.js** arquivo dentro do **index.html**

```html
<script src="./main.js"></script>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Curso de JavaScript</title>
</head>
<body>
    
    <script src="./main.js"></script>
</body>
</html>
```

- Criando o primeiro "Hello World!"

```js
alert("Hello World!");
```

![image01](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image01.png)



## #02 - Variáveis & Tipos de Dados

[Aula](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2)

### [00:00](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=0s) - Declarando variáveis com var, const & let 

- Variáveis com `var`. Não tem bloco de escopo.

```javascript
var message = "Hello World!";

alert(message);
```

![image02](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image02.png)

### [01:23](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=83s) - Diferença entre const & let 

- `const` e `let`, formas mais modernas de criar variáveis;

  - Let - Conseguimos alterar a variável depois de declarada:

  ```javascript
  let message = "Hello World!";
  
  message = "Olá Mundo!";
  
  alert(message);
  ```

  ![image05](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image05.png)

  

  - Const - **NÃO** conseguimos alterar a variável depois de declarada:

```javascript
const message = "Hello World!";

alert(message);
```

![image03](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image03.png)



```javascript
const message = "Hello World!";

message = "Olá Mundo!";

alert(message);
```

![image04](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image04.png)



### [02:52](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=172s) - Entendendo Strings 

- Strings - Textos

  - Método **Length** - Quantidade de caracteres numa string:

  ```js
  const message = "Hello World!";
  
  console.log(message.length)
  ```

  ![image06](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image06.png)

  

  - Concatenar string:

  ```javascript
  const firstName = "Thiago";
  const lastName = "da Silva";
  
  console.log("Meu nome é " + firstName + " " + lastName);
  ```

  ![image07](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image07.png)

  Usando **Template Strings**:

  ```js
  
  const firstName = "Thiago";
  const lastName = "da Silva";
  
  console.log("Meu nome é " + firstName + " " + lastName);
  console.log(`Meu nome é ${firstName} ${lastName}`);
  ```

  ![image08](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image08.png)

  

  - **toUpperCase** - string em maiúsculo, **toLowerCase** - string em minúsculo:

  ```js
  const firstName = "Thiago";
  const lastName = "da Silva";
  
  console.log("Meu nome é " + firstName + " " + lastName);
  console.log(`Meu nome é ${firstName.toUpperCase()} ${lastName.toLowerCase()}`);
  ```

  ![image09](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image09.png)

  

  - **Split** - separando uma string:

  ```js
  
  const firstName = "Thiago";
  const lastName = "da Silva";
  
  console.log("Meu nome é " + firstName + " " + lastName);
  console.log(`Meu nome é ${firstName.toUpperCase()} ${lastName.toLowerCase()}`);
  
  const names = "Pedro, Thiago, João";
  
  console.log(names.split(", "));
  ```

  ![image10](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image10.png)



### [08:15](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=495s) - Entendendo Numbers 

- Números

```js
const number = 5;

console.log(number);
```

![image11](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image11.png)

- Realizando operações matemáticas:

```js
const number = 5;

console.log(number);
console.log(number + 10);
console.log(number - 2);
console.log(number * 4);
console.log(number / 2);
```

![image12](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image12.png)



- **typeof** - verficando o tipo de variável:

```js
const number = 5;

console.log(typeof number);
console.log(typeof number.toString());
```

![image13](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image13.png)



### [09:16](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=556s) - Entendendo Booleans 

- Booleanos - False ou True (Falso ou verdadeiro):

```js
const fisrtSentence = 5 == 4;
const secondSentence = 5 == 5;

console.log(typeof fisrtSentence);
console.log(fisrtSentence);

console.log(typeof secondSentence);
console.log(secondSentence);
```

![image14](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image14.png)



### [10:11](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=611s) - Entendendo Null & Undefined 

- **null** - Variável vazia. **undefined** - Variável não definida:

```js
const x = null;
const y = undefined;

console.log(x);
console.log(y);
```

![image15](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image15.png)



### [11:20](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=680s) - Introdução a Listas & Objetos

**Lista** - Variável que guarda vários valores

**Objetos** - Variável que guarda propriedades e valores:

```js
const list = [1, 4, 3, 7, 6];
const object = {name: "Thiago"}

console.log(list);
console.log(object);
```

![image16](/home/th/Documents/DICAS_PARA_DEVS/Curso de JavaScript/images/image16.png)



## #03 - Listas

[**Aula**](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3)

### [00:00](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=0s) - Criando uma lista



### [01:56](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=116s) - Acessando elementos de uma lista



### [02:51](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=171s) - Adicionando elementos em uma lista



### [04:50](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=290s) - Removendo valores  de uma lista



### [06:05](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=365s) - Alterando valores de uma lista



### [07:19](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=439s) - Verificando índices de elementos



### [09:32](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=572s) - Verificando quantidade de elementos



### [10:31](https://www.youtube.com/watch?v=hxGIfI6n6yE&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=3&t=631s) - Verificando se uma variável é uma lista

