# 9 - Responsividade e Media Queries

## 1. Conceito de Design Responsivo

O design responsivo é uma abordagem de design que visa garantir que o layout e o conteúdo de um site sejam exibidos de forma otimizada em uma variedade de dispositivos e tamanhos de tela. Em vez de criar versões separadas para desktop e dispositivos móveis, o design responsivo ajusta automaticamente o layout com base nas dimensões da tela.

**Vantagens:**

- Melhora a experiência do usuário em diferentes dispositivos.
- Reduz a necessidade de manutenção, pois um único design se adapta a vários tamanhos de tela.
- Melhora o SEO, pois motores de busca favorecem sites com design responsivo.

## 2. Media Queries: Sintaxe e Uso

As media queries são uma ferramenta fundamental no design responsivo, permitindo que diferentes estilos CSS sejam aplicados com base nas características do dispositivo, como largura da tela, altura, resolução, etc.

### Sintaxe Básica

```css
@media (min-width: 768px) {
  /* Estilos aplicados para dispositivos com largura mínima de 768px */
  body {
    font-size: 18px;
  }
}
```

### Uso Comum

- **min-width** e **max-width**: Aplica estilos com base na largura mínima ou máxima da tela.
- **orientation**: Detecta a orientação do dispositivo (paisagem ou retrato).
- **resolution**: Aplica estilos com base na densidade de pixels do dispositivo.

```css
/* Exemplo: Ajustar o layout para telas pequenas */
@media (max-width: 600px) {
  .container {
    flex-direction: column;
  }
}
```

## 3. Layouts Fluidos e Imagens Responsivas

### Layouts Fluidos

Layouts fluidos utilizam unidades relativas, como porcentagens, em vez de unidades fixas (como pixels), permitindo que os elementos se ajustem de acordo com o tamanho da tela.

```css
.container {
  width: 100%;
  padding: 2%;
}
```

### Imagens Responsivas

Imagens responsivas se ajustam automaticamente ao tamanho do seu contêiner, garantindo que não ultrapassem as dimensões da tela.

```css
img {
  max-width: 100%;
  height: auto;
}
```

## 4. Unidades Relativas para Responsividade

### Unidades Relativas

Unidades relativas, como `%`, `em`, `rem`, `vw`, e `vh`, são cruciais para a criação de layouts responsivos, pois se adaptam ao tamanho do contêiner ou viewport.

- **%**: Relativa ao elemento pai.
- **em**: Relativa ao tamanho da fonte do elemento pai.
- **rem**: Relativa ao tamanho da fonte raiz (geralmente o `html`).
- **vw**: 1% da largura do viewport.
- **vh**: 1% da altura do viewport.

```css
.container {
  width: 80vw; /* 80% da largura do viewport */
  font-size: 1.2rem; /* 1.2 vezes o tamanho da fonte raiz */
}
```

## Prática

<html>
  <style>
    .menu {
      background-color: #333;
      padding: 10px;
      text-align: center;
      display: flex;
      flex-direction: column;
    }

    .menu a {
      color: #fff;
      padding: 10px;
      transition: background-color 0.3s;
    }

    .menu a:hover {
      background-color: #555;
    }

    @media (min-width: 1092px) {
      .menu {
        flex-direction: row;
        justify-content: center;
      }
    }

  </style>
  <body>
    <nav class="menu">
      <a href="##">Página Inicial</a>
      <a href="##">Sobre</a>
      <a href="##">Serviços</a>
      <a href="##">Contato</a>
    </nav>
  </body>
</html>

O exemplo acima possui o seguinte html:

```html
<html>
  <style>
    .menu {
      background-color: #333;
      padding: 10px;
      text-align: center;
      display: flex;
      flex-direction: column;
    }

    .menu a {
      color: #fff;
      padding: 10px;
      transition: background-color 0.3s;
    }

    .menu a:hover {
      background-color: #555;
    }

    @media (min-width: 1092px) {
      .menu {
        flex-direction: row;
        justify-content: center;
      }
    }
  </style>
  <body>
    <nav class="menu">
      <a href="##">Página Inicial</a>
      <a href="##">Sobre</a>
      <a href="##">Serviços</a>
      <a href="##">Contato</a>
    </nav>
  </body>
</html>
```
