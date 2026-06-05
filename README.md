# SQL: Projeto LojaSQL

## Sobre o Projeto

O **LojaSQL** é um projeto prático desenvolvido para aprimorar minhas habilidades em SQL Server, com foco em consultas analíticas e manipulação de dados relacionais.

O banco de dados simula o cenário de uma loja, permitindo realizar análises de vendas, comportamento de clientes e desempenho de produtos.

O objetivo é evoluir progressivamente desde conceitos fundamentais (GROUP BY, JOIN, HAVING) até consultas mais avançadas com Subqueries e Window Functions.

---

## Objetivos Técnicos

- Criar estrutura relacional com chaves primárias e estrangeiras
- Praticar `GROUP BY`, `HAVING` e `JOIN`
- Trabalhar com Subqueries
- Aplicar Window Functions:
  - `ROW_NUMBER()`
  - `RANK()`
  - `DENSE_RANK()`
  - `LAG()`
  - `OVER()`
- Implementar análises temporais (running total)
- Calcular participação percentual dentro de categorias
- Organizar consultas de forma estruturada e escalável
- Evoluir para uso de `WITH (CTE)` para modularização das queries

---

## Estrutura do Repositório
```
LojaSQL/
│
├── database/
│   ├── 01_creating_tables.sql
│   └── 02_inserting_data.sql
│
├── exercises/
│   ├── 01_GROUP_BY_basico.sql
│   ├── 02_HAVING_simples.sql
│   ├── 03_HAVING_com_multiplas_condicoes.sql
│   ├── 04_JOIN_com_GROUP_BY.sql
│   ├── 05_HAVING_com_JOIN.sql
│   ├── 06_Subqueries.sql
│   ├── 07_Ranking_manual.sql
│   └── 08_WINDOW_Functions.sql
│
└── README.md
```

## Organização das Pastas

### database/

Contém os scripts responsáveis pela estrutura e carga inicial do banco:

- **01_creating_tables.sql** → Criação das tabelas e definição dos relacionamentos.
- **02_inserting_data.sql** → Inserção de dados para permitir análises.

---

### exercises/

Contém as consultas organizadas por nível de complexidade.

A numeração representa uma progressão técnica, iniciando com agregações básicas e evoluindo até análises mais avançadas com Window Functions.

Essa organização demonstra evolução estruturada de aprendizado e clareza na separação de conceitos.

---

## Modelo de Dados

O banco segue uma estrutura relacional simples:

- Um cliente pode realizar vários pedidos.
- Um pedido pode conter vários itens.
- Cada item está vinculado a um produto.
- Produtos possuem categoria e preço.

Relacionamentos principais:

- `clientes (1) → (N) pedidos`
- `pedidos (1) → (N) itens_pedido`
- `produtos (1) → (N) itens_pedido`
