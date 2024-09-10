# 10 - Boas Práticas e Otimização

## 1. Estruturação e Organização de CSS: Módulos e BEM (Block Element Modifier)

### Módulos CSS

A modularização do CSS envolve a divisão do código em arquivos menores e reutilizáveis. Isso ajuda a manter o código organizado, reduz a duplicação e facilita a manutenção.

- **Módulos CSS**: Arquivos separados que contêm estilos específicos para uma parte da interface, como botões, formulários ou layouts.

### BEM (Block Element Modifier)

BEM é uma metodologia que facilita a criação de componentes reutilizáveis e mantém a consistência no código CSS. Ele utiliza uma convenção de nomenclatura para classes CSS.

- **Bloco**: Representa um contêiner ou componente independente (`.menu`).
- **Elemento**: Representa uma parte do bloco, que não faz sentido fora dele (`.menu__item`).
- **Modificador**: Representa uma variação ou estado do bloco ou elemento (`.menu__item--active`).

```css
/* Bloco */
.button {
  background-color: blue;
  color: white;
}

/* Modificador */
.button--large {
  padding: 10px 20px;
}
```

## 2. Minificação e Compressão de Arquivos CSS

A minificação é o processo de remover espaços em branco, comentários e outros caracteres desnecessários de arquivos CSS para reduzir seu tamanho. Isso melhora o tempo de carregamento da página.

**Ferramentas de Minificação**

- **CSSNano**: Uma ferramenta que otimiza o CSS para produção, reduzindo seu tamanho.
- **UglifyCSS**: Outra ferramenta para minificar CSS.

```bash
# Exemplo de minificação usando CSSNano
cssnano styles.css styles.min.css
```

A compressão de arquivos CSS envolve o uso de algoritmos de compactação (como Gzip) para reduzir ainda mais o tamanho do arquivo transferido entre o servidor e o navegador.

## 3. Ferramentas de Desenvolvimento: DevTools, Linting, Pré-processadores (Sass)

### DevTools

Os DevTools dos navegadores são essenciais para depurar e testar o CSS diretamente na página web. Eles permitem inspecionar elementos, modificar estilos e ver as mudanças em tempo real.

- **Inspecionar Elemento**: Ver e editar o CSS de um elemento específico.
- **Network**: Monitorar o carregamento de arquivos CSS e outros recursos.

### Linting

Linting é o processo de analisar o código para encontrar problemas de sintaxe ou estilo que podem levar a bugs ou inconsistências. Ferramentas como Stylelint ajudam a garantir que o código siga padrões estabelecidos.

```bash
# Exemplo de uso do Stylelint
stylelint 'src/**/*.css' --fix
```

### Pré-processadores (Sass)

Sass é um pré-processador CSS que permite o uso de variáveis, aninhamento, mixins, e outras funcionalidades que não estão disponíveis no CSS puro. O código Sass é compilado em CSS para uso em produção.

```scss
$primary-color: blue;

.button {
  background-color: $primary-color;
  color: white;

  &:hover {
    background-color: darken($primary-color, 10%);
  }
}
```

## 4. Acessibilidade em CSS

Acessibilidade em CSS refere-se a técnicas para garantir que o conteúdo web seja acessível a todos, incluindo pessoas com deficiências. Isso envolve considerar como os estilos afetam a navegação por teclado, leitores de tela e outras tecnologias assistivas.

### Boas Práticas

- **Contraste de Cores**: Assegure que há contraste suficiente entre o texto e o fundo para facilitar a leitura.
- **Foco Visível**: Garanta que os elementos interativos tenham um estado de foco visível.
- **Tamanhos Flexíveis**: Use unidades relativas para que os usuários possam redimensionar o texto sem quebrar o layout.

```css
/* Exemplo de foco visível */
a:focus {
  outline: 2px solid #00f;
}
```

### Ferramentas de Acessibilidade

- **Axe DevTools**: Extensão para navegadores que ajuda a identificar e corrigir problemas de acessibilidade.
- **WAVE**: Outra ferramenta popular para avaliação de acessibilidade.

# Prática

Utilizando o html que foi criado como prática em [9 - Responsividade e Media Queries](./09-responsividade-e-media-queries.md#pratica), foram implementadas algumas melhorias.

- **BEM (Block Element Modifier)**: Alterado a classe dos itens do menu para `menu__item`.
- **Módulos**: O CSS foi organizado de maneira modular, com estilos específicos para o bloco `.menu` e seus elementos `.menu__item`.
- **Acessibilidade**: Adicionado ao `<nav>` e aos `<a>` o `aria-label` melhorando a acessibilidade para usuários de tecnologias assistivas.

<html>
  <style>
    .menu {
      background-color: #333;
      padding: 10px;
      text-align: center;
      display: flex;
      flex-direction: column;
    }

    .menu__item {
      color: #fff;
      padding: 10px;
      transition: background-color 0.3s;
    }

    .menu__item:hover {
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
    <nav class="menu" aria-label="Menu de navegação">
      <a href="##" class="menu__item" aria-label="Ir para a página inicial"
        >Página Inicial</a
      >
      <a href="##" class="menu__item" aria-label="Ir para a seção Sobre"
        >Sobre</a
      >
      <a href="##" class="menu__item" aria-label="Ir para a seção de Serviços"
        >Serviços</a
      >
      <a href="##" class="menu__item" aria-label="Ir para a seção de Contato"
        >Contato</a
      >
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

    .menu__item {
      color: #fff;
      padding: 10px;
      transition: background-color 0.3s;
    }

    .menu__item:hover {
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
    <nav class="menu" aria-label="Menu de navegação">
      <a href="##" class="menu__item" aria-label="Ir para a página inicial"
        >Página Inicial</a
      >
      <a href="##" class="menu__item" aria-label="Ir para a seção Sobre"
        >Sobre</a
      >
      <a href="##" class="menu__item" aria-label="Ir para a seção de Serviços"
        >Serviços</a
      >
      <a href="##" class="menu__item" aria-label="Ir para a seção de Contato"
        >Contato</a
      >
    </nav>
  </body>
</html>
```
