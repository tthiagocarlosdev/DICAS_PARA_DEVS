# CSS Grid

Cursos CSS Grid do **Felipe Rocha** do canal dicasparadevs.

Link do curso - [link](https://www.youtube.com/watch?v=j_fzKbfH7W4)

## [0:00](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=0s) — Introdução

CSS Grid é um modelo de layout, forma de fazer layout HTML.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title> CSS Grid </title>
</head>
<body>
  <div class="container">
    <div class="box box-1"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-2"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-3"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
  </div>
</body>
</html>
```

```css
* {
  box-sizing: border-box;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.box {
  background-color: #bdbdbd;
  border: 2px solid #333;
  padding: 10px;
}
```

## [1:27](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=87s) — Criando o grid container 

```css
.container {
  display: grid;
}
```

## [01:42](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=102s) — grid-template-columns

Define as colunas que o nosso container irá ter:

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px 100px;
}
```

![grid-template-columns](https://user-images.githubusercontent.com/76978748/192115033-1efd4be3-f73c-479d-9c89-49393024b32c.png)

Podemos utilizar também porcentagem que é até melhor do que px, pois px não é responsivo:

```css
.container {
  display: grid;
  grid-template-columns: 25% 25% 50%;
}
```

![grid-template-columns-porcentagem](https://user-images.githubusercontent.com/76978748/192115046-d64098b3-66be-46c8-a2d9-9a0509355fd8.png)

Porém a medida principal que é usada é o **fr** (fração):

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

![grid-template-columns-fr](https://user-images.githubusercontent.com/76978748/192115050-57023c7b-6f3d-475e-a94a-5852841fdb1a.png)

Outra forma: 

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

![grid-template-columns-repeat](https://user-images.githubusercontent.com/76978748/192115062-303dd0b0-60f4-431d-ab36-cef2e8c096b2.png)

### Ajustando HTML para aplicar a propriedade grid-template-rows

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title> CSS Grid </title>
</head>
<body>
  <div class="container">
    <div class="box box-1"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-2"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-3"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-1"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-2"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-3"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-1"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-2"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
    <div class="box box-3"> Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo, corrupti!</div>
  </div>
</body>
</html>
```

## [04:45](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=285s) — grid-template-rows

- **grid-template-rows** define as **linhas**. Podemos usar as mesmas medidas que usamos no **grid-template-columns**.

Antes, vamos colocar um **height** para que o container ocupe toda a tela.

```css
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr 2fr 1fr;
}
```

image - grid-template-rows

```css
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
```

image - grid-template-rows-repeat

## [05:51](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=351s) — grid-gap, grid-column-gap e grid-row-gap

- **grid-gap** cria uma margem por volta dos itens:

```css
.container {
  display: grid;
  height: 100vh;

  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);

  grid-gap: 10px;
}
```

image - grid-gap

- **grid-row-gap** cria uma margem apenas entre as linhas:

```css
.container {
  display: grid;
  height: 100vh;

  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);

  grid-row-gap: 10px;
}

```

image - grid-row-gap

- **grid-column-gap** cria uma margem apenas entre as colunas:

```css
.container {
  display: grid;
  height: 100vh;

  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);

  grid-column-gap: 10px;
}
```

image - grid-column-gap

## [06:32](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=392s) — grid-auto-rows

- **grid-auto-rows** define a altura da linha. importante lembrar que se o **grid-template-row** estiver declarado, talvez o **grid-auto-rows**  não apresnte mudança:

```css
.container {
  display: grid;
  height: 100vh;

  grid-template-columns: repeat(3, 1fr);

  grid-gap: 10px;
  grid-auto-rows: 200px;
}
```

image - grid-auto-rows

```css
.container {
  display: grid;
  height: 100vh;

  grid-template-columns: repeat(3, 1fr);

  grid-gap: 10px;
  grid-auto-rows: 50px;
}
```

image - grid-auto-rows-nao-responsivo

Uma forma de declarar o **grid-auto-rows** responsivo:

```css
.container {
  display: grid;

  grid-template-columns: repeat(3, 1fr);

  grid-gap: 10px;
  grid-auto-rows: minmax(50px, auto);
}
```

image - grid-auto-rows-minmax

image - grid-auto-rows-minmax-2

Importante lembrar que o **auto** será relativo ao **height**.

## [09:35](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=575s) — grid-column

HTML para o grid-column:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title> CSS Grid </title>
</head>
<body>
  <div class="container">
    <div class="box box-1"> Box 1</div>
    <div class="box box-2"> Box 2</div>
    <div class="box box-3"> Box 3</div>
    <div class="box box-4"> Box 4</div>
    <div class="box box-5"> Box 5</div>
    <div class="box box-6"> Box 6</div>
  </div>
</body>
</html>
```

Define a coluna que o item inicia e termina, levando em consideração as linhas:

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;
}

.box-1 {
  grid-column: 1/4;
}

.box-2 {
  grid-column: 1/3;
}

.box-4 {
  grid-column: 1/4;
}

.box-6 {
  grid-column: 2/4;
}
```

image - grid-column

Os itens que não têm o grid-column definido, são jogados para baixo.

## [12:32](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=752s) — grid-row

Define a linha que o item inicia e termina:

```css
* {
  box-sizing: border-box;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

body {
  margin: 1rem;
}

.box {
  background-color: #bdbdbd;
  border: 2px solid #333;
  padding: 10px;
}

.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;
}

.box-1 {
  grid-row: 1/3;
}

```

image - grid-row

```css
.box-1 {
  grid-row: 1/3;
}

.box-4 {
  grid-row: 2/4;
}
```

image - grid-row-box4

## [15:53](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=953s) — grid-template-areas

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title> CSS Grid </title>
</head>
<body>
  <div class="container">
    <div class="box box-1"> Box 1</div>
    <div class="box box-2"> Box 2</div>
    <div class="box box-3"> Box 3</div>
    <div class="box box-4"> Box 4</div>
  </div>
</body>
</html>
```

- **grid-template-areas** desenhamos nosso layout no CSS:

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;
  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
}

.box-2 {
  grid-area: box-2;
}

.box-3 {
  grid-area: box-3;
}
.box-4 {
  grid-area: box-4;
}
```

image - grid-template-areas

## [18:06](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1086s) — grid-area

identificar cada grid para o grid-template-areas:

```css
.box-1 {
  grid-area: box-1;
}

.box-2 {
  grid-area: box-2;
}

.box-3 {
  grid-area: box-3;
}
.box-4 {
  grid-area: box-4;
}
```

## [22:01](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1321s) — align-items

Alinha os itens na vertical e execeto a propriedade **stretch** o item só vai ocupar a altura que ele precisa:

- align-items: stretch (padrão)

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - align-items-stretch 

- align-items: center

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: center;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - align-items-center

- align-items: start

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: start;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - align-items-start

- align-items: end

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: end;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - align-items-end

## [23:56](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1436s) — justify-items

Alinha os itens na horizontal e execeto a propriedade **stretch** o item só vai ocupar a largura que ele precisa:

- justify-items: stretch

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - justify-items-stretch

- justify-items: center

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: center;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - justify-items-center

- justify-items: start

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: start;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - justify-items-start

- justify-items: end

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: end;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}
```

image - justify-items-end

## [25:33](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1533s) — align-self

Alinha apenas o item que foi aplicado:

- align-self: start

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
  align-self: start;
}
```

image - align-self-start

- align-self: center

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
  align-self: center;
}
```

image - align-self-center

- align-self: end

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
  align-self: end;
}
```

image - align-self-end

## [25:56](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1556s) — justify-self

Alinha apenas o item que foi aplicado:

- justify-self: start;

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
  align-self: end;
  justify-self: start;
}

```

image - justify-self-start

- justify-self: center;

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
  align-self: center;
  justify-self: center;
}
```

image - justify-self-center;

- justify-self: end;

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px;

  align-items: stretch;
  justify-items: stretch;

  grid-template-areas: 
    'box-1 box-1 box-1'
    'box-2 box-2 box-3'
    'box-2 box-2 box-3'
    'box-4 box-4 box-4';
}

.box-1 {
  grid-area: box-1;
  align-self: center;
  justify-self: end;
}
```

image - justify-self-end;

## [26:21](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1581s) — Conclusão

Visite [css-tricks](https://css-tricks.com/snippets/css/complete-guide-grid/) para um guia mais completo de CSS Grid.
