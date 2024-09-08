# 6 - Flexbox

O Flexbox é um modelo de layout em CSS que facilita a distribuição de espaço e o alinhamento dos itens dentro de um container, tornando a criação de layouts responsivos muito mais simples.

## 1. Container Flex e Itens Flex

- **Container Flex**: Um container flex é o elemento pai ao qual aplicamos a propriedade `display: flex;`.
  
- **Itens Flex**: São os elementos filhos dentro do container flex. Eles são controlados pelas propriedades do Flexbox para definir o comportamento de layout.

## 2. Propriedades do Container

### 2.1. `flex-direction`

Define a direção em que os itens flexíveis são colocados no container.

- **Valores**: `row` (padrão), `row-reverse`, `column`, `column-reverse`.

```css
.container {
    display: flex;
    flex-direction: row;
}
```

### 2.2. `justify-content`

Alinha os itens ao longo do eixo principal do container.

- **Valores**: `flex-start` (padrão), `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.

```css
.container {
    display: flex;
    justify-content: center;
}
```

### 2.3. `align-items`

Alinha os itens ao longo do eixo transversal (perpendicular) do container.

- **Valores**: `stretch` (padrão), `flex-start`, `flex-end`, `center`, `baseline`.

```css
.container {
    display: flex;
    align-items: flex-start;
}
```

### 2.4. `flex-wrap`

Define se os itens devem quebrar para uma nova linha quando não houver espaço suficiente.

- **Valores**: `nowrap` (padrão), `wrap`, `wrap-reverse`.

```css
.container {
    display: flex;
    flex-wrap: wrap;
}
```

## 3. Propriedades dos Itens

### 3.1. `flex-grow`

Define a capacidade de um item de crescer em relação aos outros itens no container.

- **Valores**: Um número positivo (0 é o padrão, significando que o item não crescerá).

```css
.item {
    flex-grow: 1;
}
```

### 3.2. `flex-shrink`

Define a capacidade de um item de encolher se necessário.

- **Valores**: Um número positivo (1 é o padrão, significando que o item pode encolher).

```css
.item {
    flex-shrink: 2;
}
```

### 3.3. `flex-basis`

Define o tamanho inicial do item antes de ele ser ajustado pelos valores de `flex-grow` ou `flex-shrink`.

- **Valores**: Pode ser qualquer valor de tamanho CSS (por exemplo, `auto`, `100px`, `20%`).

```css
.item {
    flex-basis: 100px;
}
```

### 3.4. `align-self`

Permite ajustar o alinhamento de um item específico de forma diferente dos outros itens do container.

- **Valores**: `auto` (padrão), `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.

```css
.item {
    align-self: center;
}
```

## 4. Prática: Criando um Layout de Galeria de Imagens com Flexbox

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galeria Flexbox</title>
    <style>
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            gap: 10px; /* Espaçamento entre as imagens */
        }
        .gallery img {
            flex-basis: 200px;
            flex-grow: 1;
            max-width: 100%;
        }
    </style>
</head>
<body>

    <div class="gallery">
        <img src="../../images/js.svg" alt="JavaScript">
        <img src="../../images/html.svg" alt="HTML">
        <img src="../../images/css.svg" alt="CSS">
    </div>

</body>
</html>

~~~html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galeria Flexbox</title>
    <style>
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            gap: 10px; /* Espaçamento */
        }
        .gallery img {
            flex-basis: 200px;
            flex-grow: 1;
            max-width: 100%;
        }
    </style>
</head>
<body>

    <div class="gallery">
        <img src="../../images/js.svg" alt="JavaScript">
        <img src="../../images/html.svg" alt="HTML">
        <img src="../../images/css.svg" alt="CSS">
    </div>

</body>
</html>
~~~