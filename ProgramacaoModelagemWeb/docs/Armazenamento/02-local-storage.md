# Local Storage

E uma forma de armazenamento de dados persistente, ou seja, os dados não serão deletados se o navegador for fechado, que permite que dados sejam salvos diretamente no navegador.

- **Guardar preferências:** Lembrar o tema que você escolheu, o idioma ou outras configurações.
- **Criar aplicativos offline:** Armazenar dados para que o app funcione mesmo sem internet.
- **Acelerar o carregamento de páginas:** Guardar informações que são usadas com frequência.

## Como funciona

Para interagir com o local storage, é necessário usar o objeto localStorage do JavaScript, o qual é uma variável global assim como o document e oferece métodos para armazenar, recuperar e excluir dados, além de permitir a limpeza completa de todo o armazenamento.

- **Chaves e valores:** Os dados são armazenados em pares de chave-valor. A chave é como um rótulo e o valor é a informação que você quer guardar.
- **Métodos:** Existem métodos para guardar (setItem), recuperar (getItem), remover (removeItem) e limpar todos os dados (clear).
- **Limitação de tamanho:** Cada navegador tem um limite de armazenamento, mas geralmente é de alguns megabytes.

**Exemplo**

```javascript 
// Guardar o nome do usuário no localStorage
localStorage.setItem('nome', 'João'); 

// Recuperar e mostrar o nome do usuário
let nomeUsuario = localStorage.getItem('nome');
console.log('Nome recuperado:', nomeUsuario); 

// Guardar a idade do usuário
localStorage.setItem('idade', '25'); 

// Recuperar e mostrar a idade
let idadeUsuario = localStorage.getItem('idade');
console.log('Idade recuperada:', idadeUsuario); 

// Remover o nome do localStorage
localStorage.removeItem('nome'); 

// Tentar recuperar o nome novamente (depois de removido)
nomeUsuario = localStorage.getItem('nome');
console.log('Após remover o nome:', nomeUsuario); 

// Limpar todos os dados do localStorage
localStorage.clear(); 

// Tentar recuperar a idade (depois de limpar o localStorage)
idadeUsuario = localStorage.getItem('idade');
console.log('Após limpar todos os dados:', idadeUsuario); 
```

## Quais são as vantagens do uso

 O localStorage permite armazenar dados diretamente no navegador, sem necessidade de enviá-los ao servidor, o que melhora o desempenho das páginas, já que não há requisições constantes. Além disso, os dados são preservados mesmo após recarregar a página ou fechar o navegador, proporcionando uma experiência contínua para o usuário. Embora só armazene strings, é possível salvar objetos JSON convertendo-os com JSON.stringify() e recuperá-los com JSON.parse(). Comparado aos cookies, o localStorage oferece mais espaço, com navegadores como Chrome e Firefox suportando até 5 MB por domínio e IE até 10 MB.

## Quais são as restrições do uso

Por ser uma ferramenta relativamente recente, o web storage ainda não é
suportado por um número de versões mais antigas do navegador e por isso os cookies ainda são o padrão para armazenar informações sobre o cliente nas interações do cliente com um servidor da web.

## Exemplo de implementação

Criar uma playlist de músicas e manter os dados mesmo quando a página for fechada, o usuário pode decidir quando atualizar ou excluir estas informações.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Exemplo Local Storage</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <p>Música:</p>
  <input type="text" id="key"><br>
  <p>Banda/Cantor:</p>
  <input type="text" id="value"><br>
  <input type="button" id="btnAdd" value="Add Storage">
  <input type="button" id="btnLimp" value="Limpar Storage"><br>
  <h3>Conteúdo do Local Storage:</h3>
  <span id="conteudo"></span>
  <script src="script.js"></script>
</body>
</html>
```

```javascript
window.addEventListener("load", function() {
    // Quando a página carregar, executa a função principal
    let chave = document.getElementById("key"); 
    let valor = document.getElementById("value");
    let salvar = document.getElementById("btnAdd");
    let limpar = document.getElementById("btnLimp"); 
    let conteudo = document.getElementById("conteudo"); 

    // Evento de clique salvar
    salvar.addEventListener("click", function() {
        let input1 = chave.value; 
        let input2 = valor.value; 
        localStorage.setItem(input1, input2); // Armazena a chave e o valor no localStorage
        exibir(); 
    });

    // Evento de clique limpar
    limpar.addEventListener("click", function() {
        localStorage.clear(); 
        exibir(); 
    });

    // Evento de mudança no localStorage (quando alterado em outra aba)
    window.addEventListener("storage", function(event) {
        let key = event.key; // Chave que foi alterada
        let newValue = event.newValue; // Novo valor da chave alterada
        let oldValue = event.oldValue; // Valor anterior da chave
        let storageArea = event.storageArea; // Área de armazenamento afetada

        // Exibe no console informações sobre a mudança
        console.log("Chave alterada: " + key);
        console.log("Novo valor: " + newValue);
        console.log("Valor antigo: " + oldValue);
        console.log("Área de armazenamento: ", storageArea);
        exibir(); // Atualiza a exibição dos dados
    });

    // Função que exibe os dados do localStorage
    function exibir() {
        let str = ""; 
        for (let i = 0, len = localStorage.length; i < len; i++) {
            let key = localStorage.key(i); 
            let valor = localStorage.getItem(key); 
            str += `${[i + 1]} . ${key} : ${valor}<br>`; 
        }

        valor.value = ""; 
        chave.value = ""; 
        conteudo.innerHTML = str; // Exibe o elemento "conteudo"
    }

    exibir(); 
});
```



