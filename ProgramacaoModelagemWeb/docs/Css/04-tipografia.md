# 4 - Tipografia

- Objetivo: Explorar como estilizar texto e escolher fontes adequadas.
## Fontes web: Font-family, fallback fonts ##
-   **Font-family** e usada para definir o tipo de fonte que sera usada no texto de um elemento HTML.
-   **fallback fonts** sao as fontes alternativas que o navegador tentara aplicar se a fonte principal nao esteja disponivel o conceito dessa fonte e importante para garantir que o conteudo seja exibido dde forma legivel.
  ## Google Fonts e fontes personalizadas. ##
- **Google Fonts** sao uma coleçao de fontes gratuitas que podem ser facilmente usadas em projetos web que permitem que desenvolvedores integrem fontes externas ao site, garantindo que elas sejam exibidas corretamente, independentemente do sistema operacional ou dispositivo do usuário.
- **fontes personalizadas** sao aquelas que permitem que você use tipos de letra específicos que não estão disponíveis por padrão nos navegadores. Isso é útil para dar um estilo único ao seu site.
- **Como usar fontes personalizadas:**
- Baixe a fonte: Primeiro, você precisa do arquivo da fonte (por exemplo, .woff2 ou .woff).
- Defina a fonte no CSS: Use a regra @font-face para dizer ao navegador onde encontrar a fonte.
- Aplique a fonte: Use a propriedade font-family para aplicar a fonte aos elementos da sua página.
- **Exemplo**:
  ```css 
  @font-face {
    font-family: 'MinhaFonte';
    src: url('caminho/para/minha-fonte.woff2') format('woff2');
     body {font-family: 'MinhaFonte', Arial, sans-serif;}

## Propriedades tipográficas: Tamanho, altura da linha (line-height), espaçamento entre letras (letter-spacing) e entre palavras (word-spacing). ##
- **Tamanho font-size** define o tamanho do texto.
  - **Exemplo**:
  ```css
  p {font-size: 16px;}
  ``` 
- **Altura da linha (line-height)** Embora não seja diretamente relacionada ao espaçamento entre letras e palavras, a propriedade line-height controla o espaço vertical entre as linhas de texto. Enfim, ao ajustá-la, podemos melhorar a legibilidade e o espaçamento geral do texto.
  - **Exemplo**:
  ```css
  .paragrafo-legivel {line-height: 1.5; /* Define a altura das linhas como 1.5 vezes o tamanho da fonte */}
  ```
- **Espaçamento entre letras (letter-spacing)** permite ajustar o espaço entre os caracteres de um texto assim podemos usar valores positivos para aumentar o espaçamento e valores negativos para reduzi-lo.
  - **Exemplo**:
  ```css
  .texto-destacado {letter-spacing: 2px; /* Aumenta o espaçamento entre as letras em 2 px */} 
  .texto-condensado {letter-spacing: -1px; /* Reduz o espaçamento entre as letras em 1 px */}

- **Palavras (word-spacing)**controla o espaço entre as palavras de um texto.
  - **Exemplo**:
  ```css
  .texto-ampla {word-spacing: 5px; /* Aumenta o espaçamento entre as palavras em 5 px */}
  .texto-compacta {word-spacing: -3px; /* Reduz o espaçamento entre as palavras em 3 px */}

## Estilização de texto: Negrito, itálico, sublinhado, alinhamento, decoração e transformação. ##
- **Negrito(font-weight)** deixa o texto em negrito 
  - **Exemplo**:
  ```css
  p{font-weight : bold;}

- **Itálico (font-style)** define um estilo no texto aqui por exemplo estamos definindo o estilo italico.
  - **Exemplo**:
  ```css
  p{font-style: italic;}

- **Sublinhado (text-decoration)** Usado para adicionar uma linha abaixo do texto.
- - **Exemplo**:
  ```css
  p{text-decoration:underline;}

- **Alinhamento (text-align)** Controla o alinhamento horizontal do texto. Os valores comuns são left (esquerda), right (direita), center (centralizado)

- **Exemplo**:
   ```css
   p{text-align: center;}
   ```
- **Decoração (text-decoration)** e usado para remover a decoração de texto, como sublinhados de links, ou para criar outros efeitos como por exemplo  **text-decoration: line-through;**  Risca o texto
 - **Exemplo**:
   ```css
   p{text-decoration: none;}`
   ```

- **Transformação (text-transform)** controla a transformação do texto em maiúsculas, minúsculas ou capitalização de cada palavra.
- **Exemplo**:
  ```css
  p{text-transform: uppercase; /*deixa o texto em maiúsculas*/}
## Prática: Criar um layout de texto para um artigo, explorando fontes e estilos. ##
<style>
body {
  font-family: 'Roboto', sans-serif;
  line-height: 1.6;
  color: white;
  background:black;
  margin: 0;
  padding: 20px;
}

header {
  text-align: center;
  margin-bottom: 20px;
}

header h1 {
  font-size: 2.5em;
  font-weight: 700;
  color:white;
  margin: 0;
}

h2 {
  font-size: 2em;
  font-weight: 600;
  color: white;
  margin-top: 20px;
  margin-bottom: 10px;
}

p {
    font-size: 1em;
  margin-bottom: 15px;
  }
.import{
    text-decoration: underline;
      color: yellow;
}
</style>
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Layout</title>
</head>
<body>
  <header>
    <h1>Bem vindo</h1>
  </header>
  
  <main>
    <h2>Texto</h2>
    <p>Paragrafo</p>

    <h2>Texto</h2>
    <p>Paragrafo</p>

    <h2>Texto</h2>
    <p class="import">Paragrafo</p>
  </main>
</body>
</html>