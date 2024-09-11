# 3 - Cores e Unidades

Objetivo: Aplicar cores e diferentes unidades de medida no CSS.

## Unidades de medida: Absolutas (px, cm) vs. relativas (em, rem, %, vw, vh).

1. **Unidades de medidas absolutas:**
 - Sao aquelas que nao alteram seu tamanho independente da largura a tela.
 - **Cm(centímetro)** e uma das medidas mais conhecidas que utiliza o sistema metrico mas e uma unidade de medida mais utilizada no mundo real pois uso dessa medida é inviável para se definir o tamanho de um texto ou título, pois 1cm pode ser muito grande para a tela de um celular.
 - **Px** é uma unidade usada principalmente em design gráfico digital, como na criação de layouts para páginas da web, aplicações e imagens. Um pixel representa um ponto minúsculo em uma tela ou monitor é amplamente utilizado para definir tamanhos de fontes, margens, larguras, alturas e outros elementos de layout.
2. **Unidades de medidas relativas:**
- Essas unidades de medidas praticamente dominam as declarações em css por serem de facil adaptção a diferentes tamanhos de tela.
- **Em** no CSS é relativa ao tamanho da fonte do elemento pai. Se o pai tem uma fonte de 16px, 1em será igual a 16px. Alterar o tamanho da fonte do pai ajusta todas as medidas em Em nos elementos filhos, tornando o layout escalável e responsivo.
- **Rem** e uma das unidades mais utilizadas no desenvolvimento e front-end é uma unidade de medida em CSS baseada no tamanho da fonte do elemento raiz (:root). Normalmente, 1rem é igual a 16px. Alterar o valor da fonte no root ajusta todas as medidas em rem, tornando o design mais adaptável a diferentes tamanhos de tela.
- **Porcentagem (%)** é amplamente utilizada quando trabalhamos com css porque ela se ajusta o tamanho dos elementos de forma proporcional ao seu elemento pai. Por exemplo, ao definir 100% de largura, o elemento ocupará toda a largura disponível do contêiner.
- **Vw e Vh** são relativas ao tamanho da tela do navegador:
vw (viewport width) corresponde à largura visível do navegador. 100vw significa 100% da largura da tela.
vh (viewport height) corresponde à altura visível do navegador. 100vh significa 100% da altura da tela.
3. **Conclusao**
- Unidades absolutas são úteis para precisão, mas podem dificultar a responsividade. Por outro lado, as unidades relativas permitem maior flexibilidade e adaptação em diferentes tamanhos de tela, sendo mais adequadas para layouts responsivos.
 ## Cores em CSS: Nomeadas, HEX, RGB, RGBA, HSL e HSLA.##

1. Nomeadas: Usa nomes predefinidos para cores comuns.  Exemplo: color: red;.
2. HEX: Representa cores com um código hexadecimal de seis dígitos. Exemplo: color: #ff5733;.
3. RGB: Define a cor com base na combinação de vermelho, verde e azul, com valores de 0 a 255. Exemplo: color: rgb(255, 87, 51);.
4. RGBA: Similar ao RGB, mas inclui um canal alfa para transparência, variando de 0 (transparente) a 1 (opaco). Exemplo: color: rgba(255, 87, 51, 0.5);.
5. HSL: Define a cor por matiz (0-360 graus), saturação e luminosidade (0%-100%). Exemplo: color: hsl(9, 100%, 60%);.
6. HSLA: Semelhante ao HSL, mas adiciona um canal alfa para transparência. Exemplo: color: hsla(9, 100%, 60%, 0.5);.
## Transparência e opacidade: ##
1. **Transparência** É a capacidade de um objeto ou cor permitir que a luz passe através dele. Em CSS, é controlada pelo canal alfa em cores rgba e hsla, onde valores baixos (próximos a 0) indicam maior transparência.
2. **Opaco** É a medida de quão sólido ou visível um objeto ou cor é. Em CSS, a opacidade é definida de 0 a 1, onde 0 é totalmente transparente e 1 é totalmente opaco.
## Gradientes lineares e radiais:##
   E um efeito degradê de variação de cores que podem ser aplicadas por meio de uma função CSS em elementos HTML. Basicamente, existem dois formatos de aplicação: a linear, que como o nome sugere, apresenta o efeito em forma horizontal, vertical ou inclinada; e o efeito radial, em que a cor é propagada a partir de um ponto central.
1. A função **linear-gradient()** em CSS cria um efeito degradê linear e é usada com propriedades como background-image e border-image. Ela aplica uma transição suave entre duas ou mais cores ao fundo de um elemento HTML. É necessário usar pelo menos duas cores para que o efeito funcione.
2. A função **radial-gradient()** em CSS cria um efeito de transição de cores a partir do centro de um elemento, irradiando de forma circular ou elíptica. Ao contrário do gradiente linear, que se estende em uma direção reta, o radial-gradient espalha o gradiente a partir de um ponto central.
## Código

### Prática: Criar uma paleta de cores para um site fictício, aplicando gradientes e opacidades.

<style>
*{
    color: white;
}

body {
    background: radial-gradient(circle, rgb(0, 0, 0) 0%, rgb(130, 0, 0) 100%);
    color: #333; 
  }
  header {
    background: linear-gradient(to right, rgb(0, 0, 0), rgb(130, 0, 0));
    padding: 20px;
    color: white;
    text-align: center;
   /*gradiente linear que vai de preto a vermelho escuro.*/
  }
  button {
    background-color: rgba(255, 0, 0, 0.8);
    color: rgb(0, 0, 0);
    border: 32px;
    padding: 10px 20px;
    border-radius: 5px;
    
    /*fundo vermelho com bordas arredondadas. A cor de fundo muda para vermelho sólido ao passar o cursor sobre o botão.*/
  }
  
  button:hover {
    background-color: rgb(255, 0, 0);
  }
  .highlight {
    background: linear-gradient(to right, rgb(17, 0, 255), rgba(255, 215, 0, 0.7));
    padding: 10px;
    border-radius: 5px;
    color: white;
    /* Fundo com um gradiente linear que vai de azul a amarelo claro. */
  }
</style>
 <!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Site Fictício</title>
</head>
<body>
  <header>
    <h1>Bem-vindo</h1>
   </header>
   <br>
    <section class="highlight">
     <p style="font-weight: bold;">gradiente.</p>
    </section>
    <br>
    <button>Clique Aqui</button>
  
</body>
</html>

```css
body {
    background: radial-gradient(circle, rgb(0, 0, 0) 0%, rgb(130, 0, 0) 100%);
    color: #333; 
  }
  header {
    background: linear-gradient(to right, rgb(0, 0, 0), rgb(130, 0, 0));
    padding: 20px;
    color: white;
    text-align: center;
   /*gradiente linear que vai de preto a vermelho escuro.*/
  }
  button {
    background-color: rgba(255, 0, 0, 0.8);
    color: rgb(0, 0, 0);
    border: 32px;
    padding: 10px 20px;
    border-radius: 5px;
    
    /*fundo vermelho com bordas arredondadas. A cor de fundo muda para vermelho sólido ao passar o cursor sobre o botão.*/
  }
  
  button:hover {
    background-color: rgb(255, 0, 0);
  }
  .highlight {
    background: linear-gradient(to right, rgb(17, 0, 255), rgba(255, 215, 0, 0.7));
    padding: 10px;
    border-radius: 5px;
    color: white;
    /* Fundo com um gradiente linear que vai de azul a amarelo claro. */
  }
  html 
 <!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Site Fictício</title>
  <link rel="stylesheet" href="css ex.css">
</head>
<body>
  <header>
    <h1>Bem-vindo</h1>
   </header>
   <br>
    <section class="highlight">
     <p style="font-weight: bold;">gradiente.</p>
    </section>
    <br>
    <button>Clique Aqui</button>
  
</body>
</html>
```