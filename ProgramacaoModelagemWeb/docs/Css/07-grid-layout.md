# 7 - Grid Layout
O CSS Grid é um sistema de layout em CSS que facilita a criação de layouts complexos na web. Ele permite dividir a
página em grandes regiões ou definir o relacionamento de tamanho, posição e camada entre partes de um controle baseado
em HTML.

## 1. Containers e Itens de Grid

- **Container de Grid**: Um elemento pai ao qual aplicamos a propriedade `display: grid;`. Ele se torna o grid
  container, e todos os seus filhos são transformados em grid items.

- **Itens de Grid**: São os elementos filhos dentro do container de grid. Eles são organizados em linhas e colunas de
  acordo com as definições do grid.

## 2. Definindo Colunas e Linhas

### 2.1. `grid-template-columns`

Define o número e o tamanho das colunas no grid.

- **Exemplo**: Criar três colunas, a primeira com largura fixa de 200px, a segunda ocupando o dobro da primeira, e a
  terceira ocupando o espaço restante.

```css
.container {
    display: grid;
    grid-template-columns: 200px 2fr 1fr;
}
```

### 2.2. `grid-template-rows`

Define o número e o tamanho das linhas no grid.

- **Exemplo**: Criar duas linhas, a primeira com altura fixa de 100px e a segunda ocupando o espaço restante.

```css
.container {
    display: grid;
    grid-template-rows: 100px auto;
}
```

## 3. Áreas de Grid e Alinhamento de Itens

### 3.1. Definindo Áreas de Grid

As áreas de grid permitem que você nomeie regiões do layout e posicione os itens de acordo com essas regiões.

```css
.container {
    display: grid;
    grid-template-areas: 
        "header header header"
        "main main aside"
        "footer footer footer";
    grid-template-columns: 1fr 3fr 1fr;
    grid-template-rows: 100px auto 50px;
}

.header {
    grid-area: header;
}

.main {
    grid-area: main;
}

.aside {
    grid-area: aside;
}

.footer {
    grid-area: footer;
}
```

### 3.2. Alinhamento de Itens

Você pode alinhar os itens de grid tanto horizontalmente quanto verticalmente.

- **Exemplo**: Alinhar itens no centro do container.

```css
.container {
    display: grid;
    align-items: center; /* Alinha verticalmente */
    justify-items: center; /* Alinha horizontalmente */
}
```

## 4. Prática: Desenvolvendo um Layout de Página com CSS Grid

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout CSS Grid</title>
    <style>
        .container {
            display: grid;
            grid-template-areas: 
                "header header header"
                "content content aside"
                "footer footer footer";
            grid-template-columns: 1fr 3fr 1fr;
            grid-template-rows: 100px auto 50px;
            gap: 10px; /* Espaçamento entre os itens do grid */
        }
        .header { grid-area: header; 
                  background-color: blue;
                  color: white}
        .content { grid-area: content;
                   background-color: yellow;
                   color: black }
        .aside { grid-area: aside; 
                 background-color: red; 
                 color: white}
        .footer { grid-area: footer; 
                  background-color: gray;
                  color: white}
    </style>
</head>
<body>

    <div class="container">
        <div class="header">Cabeçalho</div>
        <div class="content">Conteúdo Principal</div>
        <div class="aside">Barra Lateral</div>
        <div class="footer">Rodapé</div>
    </div>

</body>
</html>

~~~html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout CSS Grid</title>
    <style>
        .container {
            display: grid;
            grid-template-areas: 
                "header header header"
                "content content aside"
                "footer footer footer";
            grid-template-columns: 1fr 3fr 1fr;
            grid-template-rows: 100px auto 50px;
            gap: 10px; /* Espaçamento entre os itens do grid */
        }

        .header {
            grid-area: header;
            background-color: lightblue;
        }

        .content {
            grid-area: content;
            background-color: lightgreen;
        }

        .aside {
            grid-area: aside;
            background-color: lightcoral;
        }

        .footer {
            grid-area: footer;
            background-color: lightgray;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">Cabeçalho</div>
    <div class="content">Conteúdo Principal</div>
    <div class="aside">Barra Lateral</div>
    <div class="footer">Rodapé</div>
</div>

</body>
</html>
~~~