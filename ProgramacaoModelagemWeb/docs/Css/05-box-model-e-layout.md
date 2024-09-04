# 5 - Box Model e Layout

### O box model do CSS é fundamental no desenvolvimento web, pois define a aparência e a disposição dos elementos na página.

<div style="text-align:-webkit-center ">
    <div style="width: 50%">
        <img src="../../images/representacao-box-model.png">
    </div>
</div>


### Componentes do Box Model:

#### 1. Largura ( width )

#### 2. Altura ( height )

#### 3. Preenchimento Interno

* __padding-top__    - *Superior*
* __padding-right__  - *Direita*
* __padding-bottom__ - *Inferior*
* __padding-left__   - *Esquerda*
* __padding__        - *Defini o mesmo padding para todos os lados iguais*

#### 4. Bordas
* __border-width__ - *Define a lagura da borda*
* __border-style__ - *Defini o estilo da borda*
* __border-color__ - *Defini a cor da borda*

#### 5. Margens

* __margin-top__ - *Defini margin superior*
* __margin-right__ - *Defini margin para o lado direito*
* __margin-bottom__ - *Defini margin inferior*
* __margin-left__ - *Defini margin para o lado esquerdo*
* __margin__ *Defini o mesmo margin para todos os quatro lados iguais*

#### 6. Display
* __Block__
* __Inline__
* __Inline-block__

### __Exemplo 1 (Definindo Largura - width)__

<div style="background-color: blue; width: 50%">
    <h1>Box Model</h1>
     <p>
       Defini Largura
     </p>
</div>

~~~html
<div style="background-color: blue; width: 50%">
    <h1>Box Model</h1>
    <p>
        Defini Largura
    </p>
</div>
~~~

### **Exemplo 2 (Definindo Altura - height)**

<div style="background-color: blue; height: 2rem">
    <h1>Box Model</h1>
     <p>
       Defini Altura
     </p>
</div>

~~~html

<div style="background-color: blue; height: 2rem">
    <h1>Box Model</h1>
    <p>
        Defini Altura
    </p>
</div>
~~~

### __Exemplo 3 (Preenchimento Interno)__

<div style="background-color: blue; padding: 1rem">
    <h1>Box Model</h1>
     <p>
       Defini Largura
     </p>
</div>

~~~html

<div style="background-color: blue; padding: 1rem">
    <h1>Box Model</h1>
     <p>
       Defini Largura
     </p>
</div>
~~~

### __Exemplo 4 ( Bordas )__

<div style="background-color: blue; padding: 1rem">
    <h1 style="border-width: 5px;border-style: solid; border-color: #fff;">Box Model</h1>
     <p>
       Defini Borda
     </p>
</div>

~~~html

<div style="background-color: blue; padding: 1rem">
    <h1 style="border-width: 5px;border-style: solid; border-color: #fff;">Box Model</h1>
     <p>
       Defini Borda
     </p>
</div>
~~~

### __Exemplo 5 ( Margens )__
<div style="background-color: blue; margin: 10px">
    <h1>Box Model</h1>
     <p>
       Margin
     </p>
</div>

~~~html
<div style="background-color: blue; margin: 10px">
    <h1>Box Model</h1>
     <p>
       Defini Margin
     </p>
</div>
~~~

### __Exemplo 6 ( Display )__
 1. Block
    <div style="display: block;background-color: blue; margin-bottom: 0.2rem">block 1</div>
    <div style="display: block;background-color: blue; margin-bottom: 0.2rem">block 2</div>
    <div style="display: block;background-color: blue">block 3</div>
~~~html
    <div style="display: block;background-color: blue; margin-bottom: 0.2rem">block 1</div>
    <div style="display: block;background-color: blue; margin-bottom: 0.2rem">block 2</div>
    <div style="display: block;background-color: blue">block 3</div>
~~~
 2. Inline ( Ignora propriedades de largura e altura )<br>
     <div style="display: inline;background-color: blue;">Inline 1</div>
     <div style="display: inline;background-color: blue;">Inline 2</div>
     <div style="display: inline;background-color: blue;">Inline 3</div>

~~~html
     <div style="display: inline;background-color: blue;">Inline 1</div>
     <div style="display: inline;background-color: blue;">Inline 2</div>
     <div style="display: inline;background-color: blue;">Inline 3</div>
~~~

 3. Inline-block ( Respeitam as propriedades de largura e altura )<br>
     <div style="display: inline-block;background-color: blue;">Inline-block 1</div>
     <div style="display: inline-block;background-color: blue;">Inline-block 2</div>
     <div style="display: inline-block;background-color: blue;">Inline-block 3</div>
~~~html
     <div style="display: inline;background-color: blue;">Inline 1</div>
     <div style="display: inline;background-color: blue;">Inline 2</div>
     <div style="display: inline;background-color: blue;">Inline 3</div>
~~~