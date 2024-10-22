# IndexedDB

## Como é o funcionamento?

IndexedDB é um banco de dados NoSQL baseado em navegador que permite armazenar grandes quantidades de dados. Ao contrário do `localStorage` ou `sessionStorage`, IndexedDB é assíncrono, oferece suporte a transações e permite armazenar objetos estruturados (inclusive arquivos). 

O banco de dados funciona por meio de "objetos armazenados" (`object stores`), que são similares a tabelas de um banco de dados relacional, mas sem a necessidade de definir previamente um esquema rígido. As operações são feitas de forma assíncrona e envolvem o uso de transações que garantem a consistência dos dados.

A interação com o IndexedDB se dá através de uma API JavaScript, que abre conexões para o banco, inicia transações e realiza operações de leitura/gravação em índices e "object stores".

## Em que cenários essa estratégia é recomendada?

É recomendado para aplicações web que precisam:

- Armazenar grandes quantidades de dados no lado do cliente (como dados offline).
- Manter dados disponíveis mesmo quando o usuário está offline (ex.: Progressive Web Apps - PWAs).
- Realizar operações complexas de busca e manipulação de dados localmente, sem a necessidade de comunicação com o servidor a todo momento.

Exemplos incluem:

- Aplicativos offline-first.
- Jogos web que precisam armazenar o progresso do jogador localmente.
- Ferramentas de produtividade que necessitam de grandes volumes de dados disponíveis offline, como editores de texto ou planilhas.
  
## Quais são as vantagens do uso?

- **Grande capacidade de armazenamento**: IndexedDB oferece muito mais capacidade que outros métodos de armazenamento no navegador, como `localStorage`.
- **Suporte a dados complexos**: Ele permite armazenar tipos complexos, como objetos e arrays, além de dados binários (arquivos).
- **Funciona offline**: Dados podem ser acessados e manipulados sem necessidade de uma conexão com a internet.
- **Transações**: Suporte a transações, o que garante consistência dos dados durante a leitura e escrita.
- **Performance**: Operações com IndexedDB são feitas de maneira assíncrona, o que melhora a performance e evita bloqueios na interface do usuário.

## Quais são as restrições do uso?

- **Complexidade**: A API do IndexedDB é mais complexa e verbosa do que `localStorage` ou `sessionStorage`, com muitas operações envolvendo transações e eventos.
- **Compatibilidade**: Embora seja amplamente suportado pelos navegadores modernos, alguns navegadores mais antigos ou ambientes restritos podem não oferecer suporte adequado.
- **Segurança**: Assim como outras formas de armazenamento do lado do cliente, IndexedDB pode ser vulnerável se informações confidenciais forem armazenadas sem criptografia adequada.
- **Limitações por navegador**: Cada navegador pode ter limites diferentes quanto à quantidade de dados que podem ser armazenados.

## Exemplo de implementação

Exemplo de como criar e manipular dados em um banco IndexedDB.

```javascript
// Abrir (ou criar) o banco de dados
let request = indexedDB.open("meuBancoDeDados", 1);

request.onupgradeneeded = function(event) {
    let db = event.target.result;

    // Criar um object store para nossos dados
    let objectStore = db.createObjectStore("usuarios", { keyPath: "id" });

    // Criar índice baseado no nome
    objectStore.createIndex("nome", "nome", { unique: false });
};

request.onsuccess = function(event) {
    let db = event.target.result;

    // Iniciar uma transação
    let transaction = db.transaction(["usuarios"], "readwrite");

    // Obter o object store
    let objectStore = transaction.objectStore("usuarios");

    // Adicionar um novo registro
    let request = objectStore.add({ id: 1, nome: "Maria", idade: 30 });

    request.onsuccess = function() {
        console.log("Usuário adicionado com sucesso.");
    };

    request.onerror = function() {
        console.log("Erro ao adicionar usuário.");
    };
};

request.onerror = function(event) {
    console.log("Erro ao abrir o banco de dados:", event.target.errorCode);
};
```