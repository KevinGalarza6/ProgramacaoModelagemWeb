# Session Storage

O sessionStorage é uma funcionalidade do navegador que armazena dados de forma temporária, sendo apagados quando o usuário fecha a aba ou o navegador.

É similar ao localStorage, mas com a diferença de que os dados do sessionStorage expiram quando a sessão da página é fechada, enquanto os dados do localStorage não expiram.

Os Dados não são compartilhados entre abas ou janelas, mesmo quando estão acessando a mesma origem.

## Em que cenário essa estratégia é recomendada?

- **Dados de sessão:** Carrinhos de compras: Armazenar itens adicionados ao carrinho enquanto o usuário navega pela loja, permitindo que ele continue a adicionar ou remover itens sem perder o que já selecionou.

- **Formulários:** Salvar dados de formulários preenchidos parcialmente para que o usuário possa continuar a preenchê-los mais tarde, caso a página seja recarregada ou o usuário navegue para outra página.

- **Preferências do usuário:** Armazenar temporariamente as preferências do usuário durante uma sessão, como tema, idioma ou layout.

- **Dados sensíveis:** Tokens de autenticação: Em alguns casos, pode ser útil armazenar tokens de autenticação no sessionStorage para facilitar o acesso a recursos protegidos durante uma sessão. No entanto, é importante lembrar que o sessionStorage não é uma forma segura de armazenar dados confidenciais a longo prazo, pois os dados podem ser inspecionados por ferramentas de desenvolvedor.

## Quais são as vantagens do uso?

- **Privacidade:** Os dados são armazenados localmente e não são enviados para o servidor, o que pode ser importante para alguns tipos de dados.
- **Desempenho:** As operações de leitura e escrita no sessionStorage são geralmente mais rápidas do que as operações em um banco de dados.
- **Facilidade de uso:** A API do sessionStorage é simples e fácil de usar.

## Quais são as restrições do uso?

### Duração Limitada:

- **Vinculado à Sessão:** Os dados armazenados no sessionStorage são apagados automaticamente quando a sessão do navegador é encerrada. Isso ocorre ao fechar todas as abas e janelas do navegador relacionadas a esse domínio.
- **Não Persistente:** Ao contrário do localStorage, o sessionStorage não persiste os dados entre diferentes sessões.

### Limite de Armazenamento:

- **Capacidade Finita:** Embora o limite de armazenamento varie entre os navegadores, ele é geralmente menor do que o do localStorage. Exceder esse limite pode resultar em comportamentos inesperados.

### Acessibilidade Limitada:

- Ambiente do Cliente: O sessionStorage é acessível apenas no ambiente do cliente (browser). Isso significa que você não pode acessar os dados armazenados no sessionStorage a partir do servidor.

## Emplo de implementação

```javascript
<!-- Armazenando um valor no sessionStorage -->
sessionstorage.setItem("nome", "João");

<!-- Recuperando um valor do sessionStorage -->
var nomeArmazenado = sessionStorage.getItem("nome");
console.log(nomeArmazenado); <!-- Imprime "João" no console -->

<!-- Removendo um item do sessionStorage -->
sessionStorage.removeItem("nome");
```

## Exemplo Completo: Carrinho de Compras

```javascript
<!-- Função para adicionar um item ao carrinho -->
function adicionarAoCarrinho(produto) {
    let carrinho = JSON.parse(sessionStorage.getItem("carrinho")) || [];
    carrinho.push(produto);
    sessionStorage.setItem("carrinho", JSON.stringify(carrinho));
}

<!-- Função para exibir os itens do carrinho -->
function mostrarCarrinho() {
    let carrinho = JSON.parse(sessionStorage.getItem("carrinho")) || [];
    <!-- Aqui você renderizaria os itens do carrinho na sua página -->
    console.log(carrinho);
}
```

