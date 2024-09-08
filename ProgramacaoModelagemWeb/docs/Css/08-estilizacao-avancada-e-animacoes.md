# 8 - Estilização Avançada e Animações

## 1. Pseudo-classes e Pseudo-elementos

### Pseudo-classes

Pseudo-classes são palavras-chave que podem ser adicionadas a seletores para especificar um estado especial do elemento. Elas são usadas para estilizar elementos com base em seu estado dinâmico.

**Exemplos:**

- **:hover**: Aplica estilos a um elemento quando o mouse está sobre ele.
- **:focus**: Aplica estilos a um elemento que está em foco, como um campo de formulário selecionado.

```css
/* Exemplo: Muda a cor de fundo de um botão quando o mouse passa por cima */
button:hover {
  background-color: #555;
}
```

### Pseudo-elementos

Pseudo-elementos permitem estilizar partes específicas de um elemento, como a primeira linha ou a primeira letra de um parágrafo.

**Exemplos de pseudo-elementos:**

- **::before**: Insere antes do conteúdo de um elemento.
- **::after**: Insere depois do conteúdo de um elemento.
- **::first-letter**: Aplica estilos à primeira letra de um elemento.
- **::first-line**: Aplica estilos a primeira linha de um elemento.

```css
/* A primeira linha de todo elemento <p>. */
p::first-line {
  color: blue;
  text-transform: uppercase;
}
```

## 2. Animações Básicas: `@keyframes`, `animation`, `transition`

### @keyframes

Define as etapas intermediárias de uma animação CSS, permitindo criar animações complexas.

```css
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
```

### animation

A propriedade `animation` aplica uma animação a um elemento, utilizando as etapas definidas em `@keyframes`.

```css
/* Exemplo: Aplica a animação de fadeIn (criada no exemplo anterior) a uma div */
div {
  animation: fadeIn 2s ease-in-out;
}
```

### transition

Permite a transição suave entre diferentes estados de um elemento (como mudar a cor de fundo ao passar o mouse).

```css
/* Exemplo: Transição suave na cor de fundo de um botão */
button {
  background-color: #333;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #555;
}
```

## 3. Efeitos de Hover e Foco

### Efeito de Hover

O efeito de hover é aplicado quando o usuário passa o mouse sobre um elemento. Combinado com `transition`, o efeito se torna suave e agradável.

```css
/* Exemplo: Altera a cor de um link ao passar o mouse */
a {
  color: #000;
  transition: color 0.2s;
}

a:hover {
  color: #f00;
}
```

### Efeito de Foco

O efeito de foco é ativado quando um elemento, como um campo de formulário, está em foco, geralmente após ser clicado ou acessado via teclado.

```css
/* Exemplo: Altera a borda de um campo de input quando em foco */
input:focus {
  border-color: #00f;
  outline: none;
}
```

## 4. Transições Suaves e Animações Personalizadas

### Transições Suaves

As transições suaves criam uma experiência de usuário mais fluida ao mudar o estado de um elemento.

```css
/* Exemplo: Transição suave em um botão */
button {
  background-color: #008cba;
  transition: background-color 0.4s ease;
}

button:hover {
  background-color: #005f73;
}
```

### Animações Personalizadas

Animações personalizadas permitem que você crie movimentos mais complexos e interações ricas com o usuário.

```css
@keyframes slideIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

.box {
  animation: slideIn 1s ease-out;
}
```

## Prática

<html>
  <style>
    .menu {
      background-color: #333;
      padding: 10px;
      text-align: center;
    }

    .menu a {
      color: #fff;
      padding: 10px;
      transition: background-color 0.3s;
    }

    .menu a:hover {
      background-color: #555;
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
    }

    .menu a {
      color: #fff;
      padding: 10px;
      transition: background-color 0.3s;
    }

    .menu a:hover {
      background-color: #555;
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
