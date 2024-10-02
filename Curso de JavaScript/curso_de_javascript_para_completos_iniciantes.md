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

### [01:23](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=83s) - Diferença entre const & let 

### [02:52](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=172s) - Entendendo Strings 

### [08:15](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=495s) - Entendendo Numbers 

### [09:16](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=556s) - Entendendo Booleans 

### [10:11](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=611s) - Entendendo Null & Undefined 

### [11:20](https://www.youtube.com/watch?v=c_ZCzdMUlxk&list=PLm-VCNNTu3LnlPhqxx03kvjQd3qF6EBdz&index=2&t=680s) - Introdução a Listas & Objetos