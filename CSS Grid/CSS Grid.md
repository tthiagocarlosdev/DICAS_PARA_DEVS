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

![grid-template-rows](https://user-images.githubusercontent.com/76978748/192120175-bc27df89-e423-4f31-888d-9cc56c2ad640.png)

```css
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
```

![grid-template-rows-repeat](https://user-images.githubusercontent.com/76978748/192120184-01dc2be9-0f2f-465c-a7c2-063578a80faf.png)

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

![grid-gap](https://user-images.githubusercontent.com/76978748/192120192-4bde2d7d-64d2-4f92-841d-6139c95d7efb.png)

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

![grid-row-gap](https://user-images.githubusercontent.com/76978748/192120198-df5edac5-50bf-4e35-9fd2-2df73197f418.png)

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

![grid-column-gap](https://user-images.githubusercontent.com/76978748/192120211-a037ff03-f207-4ce6-a565-e505f62f0140.png)

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

![grid-auto-rows](https://user-images.githubusercontent.com/76978748/192120235-4220b55d-2f80-4d53-b75a-29afe2dcf75f.png)

```css
.container {
  display: grid;
  height: 100vh;

  grid-template-columns: repeat(3, 1fr);

  grid-gap: 10px;
  grid-auto-rows: 50px;
}
```

![grid-auto-rows-nao-responsivo](https://user-images.githubusercontent.com/76978748/192120239-199c5af6-d481-4bd6-ad70-c8a9ada7ca3f.png)

Uma forma de declarar o **grid-auto-rows** responsivo:

```css
.container {
  display: grid;

  grid-template-columns: repeat(3, 1fr);

  grid-gap: 10px;
  grid-auto-rows: minmax(50px, auto);
}
```

![grid-auto-rows-minmax](https://user-images.githubusercontent.com/76978748/192120270-6f760cee-1f64-41a8-b97f-36e798c50b00.png)

![grid-auto-rows-minmax-2](https://user-images.githubusercontent.com/76978748/192120273-71e32a1d-faa9-4e45-8034-16b40cb1dadf.png)

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

![grid-column](https://user-images.githubusercontent.com/76978748/192120281-be66e3ed-8018-4873-af14-e01c2712b5b5.png)

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

![grid-row](https://user-images.githubusercontent.com/76978748/192120288-4bbf2615-f39a-47d4-9ddd-8614e961a1c7.png)

```css
.box-1 {
  grid-row: 1/3;
}

.box-4 {
  grid-row: 2/4;
}
```

![grid-row-box4](https://user-images.githubusercontent.com/76978748/192120295-ea65fd86-d827-4f5b-ae29-fa43228484d3.png)

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

![grid-template-areas: ](https://user-images.githubusercontent.com/76978748/192120298-2be08266-3893-4c00-a7b8-bd8f10d5c4a1.png)

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

![align-items-stretch ](https://user-images.githubusercontent.com/76978748/192120319-ab54b740-b84d-4863-8d62-14c9a5afe4bf.png)

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

![align-items-center](https://user-images.githubusercontent.com/76978748/192120327-811e5535-c0fb-4ed0-92ce-9deb40e7062c.png)

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

![align-items-start](https://user-images.githubusercontent.com/76978748/192120338-6cb621eb-2023-43f3-8664-7de7fcafbe6b.png)

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

![align-items-end](https://user-images.githubusercontent.com/76978748/192120347-00fc0e63-22a4-4f0b-94bd-33f0d76161d9.png)

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

![justify-items-stretch](https://user-images.githubusercontent.com/76978748/192120354-6e8f3b99-39a2-41b5-9f6d-439362e21d4f.png)

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

![justify-items-center](https://user-images.githubusercontent.com/76978748/192120362-9415271a-7616-48a8-bad4-ba63a6a63125.png)

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

![justify-items-start](https://user-images.githubusercontent.com/76978748/192120400-b8545eb6-654f-4a5b-b8db-005929f680f7.png)

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

![justify-items-end](https://user-images.githubusercontent.com/76978748/192120405-ac6407f4-e916-47d8-a7c7-e8903c9c0a2d.png)

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

![align-self-start;](https://user-images.githubusercontent.com/76978748/192120411-f6127dc8-a717-4a41-97b8-a72c70773360.png)

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

![align-self-center](https://user-images.githubusercontent.com/76978748/192120415-c6b2fb79-e604-453f-a1b2-cacd33359d0a.png)

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

![align-self-end](https://user-images.githubusercontent.com/76978748/192120421-93efea46-fbb5-4c87-b0dd-de807e3fb467.png)

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

![justify-self-start](https://user-images.githubusercontent.com/76978748/192120438-c7e8ea42-b75f-4bd0-86eb-d139220d6c20.png)

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

![justify-self-center](https://user-images.githubusercontent.com/76978748/192120442-3158a899-f450-4adc-9ad0-79724106fdca.png)

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

![justify-self-end](https://user-images.githubusercontent.com/76978748/192120445-bca6805c-4c9f-4020-8f5f-eceeab55eecd.png)

## [26:21](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1581s) — Conclusão

Visite [css-tricks](https://css-tricks.com/snippets/css/complete-guide-grid/) para um guia mais completo de CSS Grid.
