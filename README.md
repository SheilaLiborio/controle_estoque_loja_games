# 🎮 Controle de Estoque - Loja de Games

Este projeto faz parte do **Bootcamp Porto SoulCode**.  
É um sistema de **Controle de Estoque** para uma loja de games, desenvolvido em **Python** com **SQLite** como banco de dados relacional.

---

## **Objetivo**

- 📦 Cadastrar produtos e fornecedores com validações obrigatórias.
- 🔍 Consultar o estoque por categoria e por fornecedor.
- ➕ Registrar reposições de produtos.
- 📊 Gerar relatórios de produtos com baixo estoque.
- ⚠️ Exibir alertas visuais quando o estoque estiver abaixo de 5 unidades, usando a biblioteca **Rich**.

---

## **Estrutura do Banco de Dados**

- **Tabela Produtos**
  - `id` (PK)
  - `nome` (único)
  - `preco`
  - `categoria`
  - `quantidade_estoque`
  - `fornecedor_id` (FK)

- **Tabela Fornecedores**
  - `id` (PK)
  - `nome`
  - `cnpj` (único)
  - `telefone`

- **Tabela Reposições** *(opcional)*
  - `id` (PK)
  - `id_produto` (FK)
  - `id_fornecedor` (FK)
  - `quantidade`
  - `data_reposicao`

---

## ⚙️ **Tecnologias Utilizadas**

- **Python** 🐍
  - SQLite3
  - Rich (interface de terminal)
- **SQLite** 🗃️
- **VS Code** ou **Colab** para desenvolvimento.

---

## **Validações Principais**

- Não cadastrar produtos com preço igual ou menor que zero.
- Não permitir estoque negativo.
- Nome do produto deve ser único.
- CNPJ do fornecedor deve ter 14 dígitos válidos e ser único.
- Quantidade reposta deve ser maior que zero.
- Produto sempre associado a um fornecedor existente.

---

## **Funcionalidades Extras (Desafios)**

- Relatório com os 5 produtos de menor estoque.
- Relatório de fornecedores que mais realizaram reposições.
- Histórico de alterações de preço (opcional).
- Tabelas coloridas e alertas visuais com Rich.

