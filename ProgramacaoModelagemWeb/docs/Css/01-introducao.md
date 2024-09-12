# 1 - Introdução ao CSS

## O que é CSS ?
##### O Css éa sigla para: Cascading Style Sheets, ou Folhas de Estilo em Cascata em português. Essa linguagem de estilo é fundamental para a criação de páginas web com design atraente e funcional.

## Um pouco da História do Css
##### A criação do CSS foi motivada pela necessidade de separar a estrutura (HTML) da apresentação (CSS) das páginas web. Antes do CSS, as estilizações eram inseridas diretamente no código HTML, o que tornava o código mais complexo e difícil de manter. <br> Em 1994: Håkon Wium Lie propôs a ideia do CSS, buscando uma forma mais eficiente de estilizar páginas web. <br>Em 1996: O World Wide Web Consortium (W3C) lançou a primeira versão do CSS, o CSS1. <br>Desde então: O CSS evoluiu significativamente, com novas versões introduzindo recursos mais poderosos e flexíveis.

## Estruturabásica de um arquivo em Css
### Color
<div style="color: blue">Este texto é azul.</div>

~~~html
<div style="color: blue">Este texto é azul.</div>
~~~

### background-color
<div style="background-color: lightgreen; color: black">
  Esta caixa tem um fundo verde claro.
</div>

~~~html
<div style="background-color: lightgreen; color: black">
  Esta caixa tem um fundo verde claro.
</div>
~~~


### font-size
<div style="font-size: 30px">Este texto tem 30px.</div>

~~~html
<div style="font-size: 30px">Este texto tem 30px.</div>
~~~

### font-family
<div style="font-family: 'Courier New', monospace">
  Este texto está em 'Courier New'.
</div>

~~~html
<div style="font-family: 'Courier New', monospace">
  Este texto está em 'Courier New'.
</div>
~~~

### text-align 
<div style="text-align: right">Este texto está alinhado à direita.</div>

~~~html
<div style="text-align: right">Este texto está alinhado à direita.</div>
~~~

### margin 
<div style="margin: 50px">Esta caixa tem uma margem de 50px.</div>

~~~html
<div style="margin: 50px">Esta caixa tem uma margem de 50px.</div>
~~~


### border
<div style="border: 5px solid">
  Esta caixa tem uma borda sólida de 5px.
</div>

~~~html
<div style="border: 5px solid">
  Esta caixa tem uma borda sólida de 5px.
</div>
~~~

### border-width


<div style="border: 10px solid">Esta caixa tem uma largura de borda de 10px.</div>

~~~html
<div style="border: 10px solid">Esta caixa tem uma largura de borda de 10px.</div>
~~~

### border-color


<div style="border: 2px solid orange">Esta caixa tem uma borda laranja.</div>

~~~html
<div style="border: 2px solid orange">Esta caixa tem uma borda laranja.</div>
~~~

### padding


<div style="padding: 30px">Esta caixa tem um preenchimento de 30px.</div>

~~~html
<div style="padding: 30px">Esta caixa tem um preenchimento de 30px.</div>
~~~

### width


<div style="width: 100px">Esta caixa tem uma largura de 100px.</div>

~~~html
<div style="width: 100px">Esta caixa tem uma largura de 100px.</div>
~~~

### height


<div style="height: 100px">Esta caixa tem uma altura de 100px.</div>

~~~html
<div style="height: 100px">Esta caixa tem uma altura de 100px.</div>
~~~

### z-index


<div style="z-index: 2">Esta caixa tem um z-index de 2.</div>

~~~html
<div style="z-index: 2">Esta caixa tem um z-index de 2.</div>
~~~

### overflow
<div style="overflow: scroll; height: 50px">
  Esta caixa tem um overflow de rolagem. Esta caixa tem um overflow de rolagem. Esta caixa
  tem um overflow de rolagem. Esta caixa tem um overflow de rolagem. Esta caixa tem um
  overflow de rolagem. Esta caixa tem um overflow de rolagem.
</div>

~~~html
<div style="overflow: scroll; height: 50px">
  Esta caixa tem um overflow de rolagem. Esta caixa tem um overflow de rolagem. Esta caixa
  tem um overflow de rolagem. Esta caixa tem um overflow de rolagem. Esta caixa tem um
  overflow de rolagem. Esta caixa tem um overflow de rolagem.
</div>
~~~

~~~html
~~~

~~~
### cursor
<div style="cursor: crosshair">Esta caixa tem um cursor em forma de mira.</div>

~~~html
<div style="cursor: crosshair">Esta caixa tem um cursor em forma de mira.</div>

~~~
### opacity
<div style="opacity: 0.3">Esta caixa tem uma opacidade de 0.3.</div>

~~~html
<div style="opacity: 0.3">Esta caixa tem uma opacidade de 0.3.</div>

~~~
### visibility (hidden)
<div style="visibility: hidden">Esta caixa está escondida.</div>

~~~html
<div style="visibility: hidden">Esta caixa está escondida.</div>

~~~
### visibility (visible)
<div style="visibility: visible">Esta caixa está visível.</div>

~~~html
<div style="visibility: visible">Esta caixa está visível.</div>

~~~
### font-weight
<div style="font-weight: lighter">Este texto é mais claro.</div>

~~~html
<div style="font-weight: lighter">Este texto é mais claro.</div>

~~~
### font-style
<div style="font-style: oblique">Este texto é oblíquo.</div>

~~~html
<div style="font-style: oblique">Este texto é oblíquo.</div>

~~~
### white-space
<div style="white-space: pre">Este texto tem espaços extras.</div>

~~~html
<div style="white-space: pre">Este texto tem espaços extras.</div>

~~~
### vertical-align
<div style="vertical-align: super">Este texto é super.</div>

~~~html
<div style="vertical-align: super">Este texto é super.</div>
~~~