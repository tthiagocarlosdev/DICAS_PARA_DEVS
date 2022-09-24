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

image - grid-template-columns

Podemos utilizar também porcentagem que é até melhor do que px, pois px não é responsivo:

```css
.container {
  display: grid;
  grid-template-columns: 25% 25% 50%;
}
```

image - grid-template-columns-porcentagem

Porém a medida principal que é usada é o **fr** (fração):

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

image - grid-template-columns-fr

Outra forma: 

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

image - grid-template-columns-repeat

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

PAREI

## [05:51](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=351s) — grid-gap, grid-column-gap e grid-row-gap

## [06:32](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=392s) — grid-auto-rows

## [09:35](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=575s) — grid-column

## [12:32](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=752s) — grid-row

## [15:53](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=953s) — grid-template-areas

## [18:06](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1086s) — grid-area

## [22:01](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1321s) — align-items

## [23:56](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1436s) — justify-items

## [25:33](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1533s) — align-self

## [25:56](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1556s) — justify-self

## [26:21](https://www.youtube.com/watch?v=j_fzKbfH7W4&t=1581s) — Conclusão







## Definição

Define o Grid no **container**:

```css

```

## Primeira propriedade



```css

```



