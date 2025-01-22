# Carrinho-de-Compras
Uma simulação de carrinho de compras

### Objetivo:
Criar uma lista composta por vários **dicionários** (`dict`). Cada dicionário deve representar um item do carrinho de compras.

---

### Requisitos:
1. Cada dicionário deve conter, no mínimo, as seguintes chaves:
   - **`nome`**: Nome do item.
   - **`quantidade`**: Quantidade desejada do item.(Deve ter pelo menos **2 unidades**)
   - **`preco_unitario`**: Preço de cada unidade do item.

2. A lista final deve ser composta por pelo menos **3 itens diferentes**.

---

### Exemplo:
```python

carrinho = [
    {"nome": "Calça Bege", "quantidade": 3, "preco_unitario": 52.50},
    {"nome": "Chapéu de Marinheiro", "quantidade": 10, "preco_unitario": 42.10},
    {"nome": "Mochila de Capivara", "quantidade": 5, "preco_unitario": 120.00}
]

---
### Remover o Primeiro Item 🗑️

### O que aconteceu? 🤔

Durante nossa aventura de compras, percebemos que adicionamos o primeiro item **por engano**. Talvez tenha sido o entusiasmo de ver tantas promoções, mas agora é hora de corrigir isso e remover o item errado do nosso carrinho!

---

### Passos para Remover o Primeiro Item:

1. Use o método `pop(0)` para remover o item no índice 0 (o primeiro da lista).
2. Armazene o item removido em uma variável para verificarmos qual foi excluído.
3. Atualize o carrinho para refletir a mudança.

---

### Código de Exemplo:

```python
# Carrinho de compras
carrinho = [
    {"nome": "Machado de Guerra", "quantidade": 20, "preco_unitario": 2500.50},
    {"nome": "Camiseta Legal", "quantidade": 4, "preco_unitario": 52.30},
    {"nome": "Mochila de Hyrax", "quantidade": 6, "preco_unitario": 200.00}
]

# Removendo o primeiro item
item_removido = carrinho.pop(0)

# Exibindo o carrinho atualizado
print(f"Carrinho atualizado: {carrinho}")

# Exibindo o item removido
print(f"Item removido por engano: {item_removido}")

---

## Adicionar um Novo Item 🛍️

### O que aconteceu agora? 🤔

Depois de corrigir o engano e remover o item errado, lembramos que ainda precisamos adicionar um novo item ao carrinho — agora o item **certo**! Vamos garantir que nossa lista fique completa para finalizar a compra.

---

### Passos para Adicionar um Novo Item:

1. Use o método `append()` para adicionar um novo dicionário ao final da lista do carrinho.
2. Certifique-se de que o dicionário contenha as informações básicas do item:
   - **`nome`**: Nome do produto.
   - **`quantidade`**: Quantidade desejada.
   - **`preco_unitario`**: Preço de cada unidade do item.

---

### Código de Exemplo:

```python
# Carrinho de compras atualizado
carrinho = [
    {"nome": "Caderno", "quantidade": 6, "preco_unitario": 15.00},
    {"nome": "Mochila", "quantidade": 10, "preco_unitario": 120.00}
]

# Novo item a ser adicionado
novo_item = {"nome": "Estojo", "quantidade": 1, "preco_unitario": 25.00}

# Adicionando o novo item ao carrinho
carrinho.append(novo_item)

# Exibindo o carrinho atualizado
print(f"Carrinho atualizado: {carrinho}")

---

## Checkout 🧾

Agora que já montamos nosso **carrinho de compras**, vamos calcular o **preço final** diretamente, usando variáveis para cada cálculo e arredondando os valores com `round`.

---

### Código de Exemplo:

```python
# Carrinho de compras
carrinho = [
    {"nome": "Caneta", "quantidade": 3, "preco_unitario": 1.50},
    {"nome": "Caderno", "quantidade": 5, "preco_unitario": 15.00},
    {"nome": "Mochila", "quantidade": 6, "preco_unitario": 120.00}
]

# Acessando os valores e calculando os preços
quantidade_1 = carrinho[0]["quantidade"]
preco_1 = carrinho[0]["preco_unitario"]
preco_item_1 = round(quantidade_1 * preco_1, 2)

quantidade_2 = carrinho[1]["quantidade"]
preco_2 = carrinho[1]["preco_unitario"]
preco_item_2 = round(quantidade_2 * preco_2, 2)

quantidade_3 = carrinho[2]["quantidade"]
preco_3 = carrinho[2]["preco_unitario"]
preco_item_3 = round(quantidade_3 * preco_3, 2)

# Somando os preços para obter o total
total = round(preco_item_1 + preco_item_2 + preco_item_3, 2)

# Exibindo o total final
print(f"Total: R$ {total}")
