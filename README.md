# 📚 Banco de Dados para Livraria

Este repositório contém a modelagem de um banco de dados relacional para um sistema simples de gerenciamento de pedidos de uma **livraria**. O objetivo é armazenar informações sobre os livros e os pedidos feitos pelos clientes.

## 🧱 Estrutura do Banco de Dados

### 📘 Tabela `livros`
Tabela responsável por armazenar os dados dos livros disponíveis na livraria.

| Campo     | Tipo          | Descrição                    |
|-----------|---------------|------------------------------|
| id        | INT           | Identificador do livro       |
| titulo    | VARCHAR(100)  | Título do livro              |
| autor     | VARCHAR(100)  | Nome do autor                |
| preco     | DECIMAL(10,2) | Preço do livro               |
| estoque   | INT           | Quantidade em estoque        |

### 🧾 Tabela `pedidos`
Tabela que armazena os pedidos realizados pelos clientes.

| Campo        | Tipo         | Descrição                                |
|--------------|--------------|-------------------------------------------|
| id           | INT          | Identificador do pedido                   |
| data_pedido  | DATE         | Data em que o pedido foi realizado        |
| livro_id     | INT          | ID do livro (chave estrangeira)           |
| quantidade   | INT          | Quantidade de exemplares do livro         |

Relacionamento: Cada pedido está relacionado a um livro da tabela `livros`.

## 📂 Arquivos

- `livraria.sql`: Script contendo os comandos SQL para criar as tabelas e inserir dados de exemplo.

## ▶️ Como utilizar

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/livraria-db.git
```

2. Acesse a pasta do projeto:

```bash
cd livraria-db
```

3. Execute o script SQL no seu sistema de gerenciamento de banco de dados (como MySQL, PostgreSQL ou SQLite):

```sql
-- Em um cliente SQL:
SOURCE livraria.sql;
```

## 💾 Exemplo de dados inseridos

**livros**
- Dom Casmurro, Machado de Assis
- O Pequeno Príncipe, Antoine de Saint-Exupéry
- 1984, George Orwell

**pedidos**
- Pedido do livro "Dom Casmurro" em 2025-06-01
- Pedido do livro "1984" em 2025-06-02
- Pedido do livro "O Pequeno Príncipe" em 2025-06-03

## 📝 Histórico

- `v1.0` - Criação das tabelas `livros` e `pedidos` e inserção de dados fictícios

---

## 🧑‍💻 Autor

Projeto desenvolvido como prática de modelagem de banco de dados e controle de versão com Git e GitHub.
