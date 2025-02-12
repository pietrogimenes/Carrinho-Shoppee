# Shopee - Simulação de Carrinho de Compras (Backend) 🛒

Este projeto simula um **carrinho de compras** de uma loja online (inspirado na Shopee) no **backend**, utilizando **Node.js**. A aplicação funciona via **terminal** e permite a interação com um carrinho de compras, onde você pode adicionar, remover e visualizar itens.

## Funcionalidades 📝

O carrinho de compras simula algumas das ações mais comuns em um sistema de e-commerce:

- **Adicionar item ao carrinho**: Adiciona um item com nome, preço e quantidade ao carrinho.
- **Remover item (diminui a quantidade)**: Diminui a quantidade de um item. Se a quantidade chegar a 1, o item será removido do carrinho.
- **Excluir item do carrinho**: Remove o item completamente do carrinho.
- **Visualizar o carrinho**: Exibe todos os itens presentes no carrinho, com nome, preço, quantidade e subtotal.
- **Calcular total**: Calcula e exibe o total do carrinho somando os subtotais de cada item.

## Como usar 🖥️

### Pré-requisitos 🔧

Certifique-se de ter o **Node.js** instalado. Caso não tenha, você pode baixá-lo no [site oficial](https://nodejs.org/).

### Passos para rodar o projeto 🚀

1. **Clone o repositório** para sua máquina local:

   ```bash
   git clone https://github.com/seu-usuario/shopee-cart-simulation.git
   cd shopee-cart-simulation

2. **Instale as dependências** (caso haja alguma):
npm install

3. **Execute o aplicativo:**
node index.js

Isso irá executar as funções do carrinho de compras no terminal, criando itens, removendo-os e exibindo os totais.

Estrutura do Projeto 📂
services/cart.js: Contém as funções relacionadas ao carrinho de compras (adicionar, remover, deletar itens e calcular total).
services/item.js: Contém a função para criar itens com subtotais.
index.js: Arquivo principal que orquestra a execução das funções de carrinho e itens.
Funções no cart.js ⚙️
addItem(userCart, item): Adiciona um item ao carrinho.
deleteItem(userCart, name): Deleta um item do carrinho pelo nome.
removeItem(userCart, item): Remove ou diminui a quantidade de um item no carrinho. Se a quantidade for 1, o item é removido completamente.
displayCart(userCart): Exibe todos os itens do carrinho, incluindo nome, preço, quantidade e subtotal.
calculateTotal(userCart): Calcula o valor total do carrinho somando os subtotais de todos os itens.
Funções no item.js 🛍️
createItem(name, price, quantity): Cria um item com nome, preço e quantidade, e calcula o subtotal (preço * quantidade).
Exemplo de Uso 🖋️
Criando e Manipulando o Carrinho
1. **Criação de itens:**

const item1 = await createItem("hotwheels ferrari", 20.99, 1);
const item2 = await createItem("hotwheels lamborghini", 39.99, 3);

2. **Adicionando itens ao carrinho:**
await cartService.addItem(myCart, item1);
await cartService.addItem(myCart, item2);

3. **Removendo itens do carrinho:**
 - Diminuir quantidade de um item (a quantidade vai de 3 para 2, e depois de 2 para 1):

await cartService.removeItem(myCart, item2);
await cartService.removeItem(myCart, item2);
await cartService.removeItem(myCart, item2); // item2 é removido

4. **Exibindo o carrinho:**
await cartService.displayCart(myCart);

5.**Calculando o total:**
await cartService.calculateTotal(myCart);


**Exemplo de Saída no Terminal** 📊
Após rodar as funções, a saída no terminal pode ser algo assim:

Shopee cart list:
1. hotwheels ferrari - R$ 20.99 | 1x | Subtotal = 20.99

Shopee Cart TOTAL IS:
🛒 Total: 20.99



**Observações** ⚠️
Este projeto foi desenvolvido para fins educacionais e é uma simulação simples de um carrinho de compras. Ele não tem integração com banco de dados, autenticação de usuário ou front-end, sendo focado em manipulação de dados e operações de backend utilizando Node.js.

**Contribuições** 🤝
Se você quiser melhorar ou adicionar funcionalidades ao projeto, fique à vontade para fazer um fork e enviar pull requests.
