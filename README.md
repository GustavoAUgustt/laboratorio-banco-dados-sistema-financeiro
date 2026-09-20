# Laboratório de Banco de Dados — Sistema de Controle Financeiro

## 📌 Projeto

Projeto acadêmico da disciplina **Laboratório de Banco de Dados**, com o tema **Sistema de Controle Financeiro**.

A proposta é desenvolver a modelagem e implementação de um banco de dados capaz de centralizar e organizar informações financeiras pessoais, permitindo o gerenciamento de bancos, contas, cartões de crédito, transações, categorias, faturas, compras parceladas, investimentos, orçamentos e movimentações recorrentes.

O sistema foi pensado como uma solução de gestão financeira pessoal, inspirada no funcionamento de aplicações de controle financeiro, permitindo acompanhar o fluxo de caixa, compromissos futuros e patrimônio financeiro.

---

## 🎯 Objetivo

Projetar e implementar um banco de dados relacional que represente de forma consistente a vida financeira de um usuário, mantendo a integridade dos dados e possibilitando consultas simples e analíticas.

O projeto deverá contemplar as etapas:

- Modelagem conceitual;
- Modelagem lógica;
- Modelagem física;
- Implementação do banco de dados;
- População das tabelas;
- Consultas SQL;
- Atualização e manipulação dos dados.

---

## 💰 Escopo do Sistema

O sistema deverá permitir o cadastro e gerenciamento de:

### 👤 Usuários
Representação dos usuários que utilizarão o sistema e serão responsáveis pelos seus recursos financeiros.

### 🏦 Bancos e Instituições Financeiras
Cadastro de diferentes instituições financeiras nas quais o usuário possui relacionamento.

Exemplos:

- Nubank;
- Itaú;
- Banco Inter;
- Caixa;
- Banco do Brasil.

### 💳 Contas
Um usuário poderá possuir várias contas, inclusive em diferentes instituições.

Exemplos de tipos:

- Conta corrente;
- Conta poupança;
- Carteira/dinheiro em espécie.

As contas poderão possuir informações como saldo, tipo, moeda, situação e datas relevantes.

### 💳 Cartões de Crédito
Cadastro de cartões vinculados às instituições/contas do usuário.

Informações previstas:

- Bandeira;
- Identificação do cartão;
- Limite total;
- Limite disponível;
- Dia de fechamento;
- Dia de vencimento;
- Situação.

### 🧾 Faturas
Cada cartão poderá possuir diversas faturas, normalmente relacionadas aos seus ciclos mensais.

A fatura deverá permitir o controle de:

- Período da fatura;
- Data de fechamento;
- Data de vencimento;
- Valor total;
- Valor pago;
- Status.

Possíveis status:

- Aberta;
- Fechada;
- Paga;
- Parcialmente paga;
- Atrasada.

### 💰 Transações
Registro das movimentações financeiras realizadas pelo usuário.

Tipos principais:

- Receita;
- Despesa;
- Transferência interna.

Cada movimentação poderá possuir:

- Valor;
- Data;
- Descrição;
- Tipo;
- Status;
- Conta de origem;
- Conta de destino, quando aplicável;
- Categoria;
- Forma de pagamento.

As transferências entre contas próprias deverão ser diferenciadas de receitas e despesas para não distorcer o fluxo de caixa.

### 🗂️ Categorias e Subcategorias
Organização das receitas e despesas em uma estrutura hierárquica.

Exemplos:

- Alimentação
  - Restaurante
  - Delivery
  - Mercado
- Transporte
  - Uber
  - Combustível
  - Transporte público
- Lazer
  - Cinema
  - Jogos
  - Viagens
- Moradia
  - Aluguel
  - Energia
  - Internet

Essa estrutura deverá permitir consultas e relatórios agrupados por categoria e subcategoria.

### 🛒 Compras Parceladas
O sistema deverá representar compras realizadas no cartão de crédito que sejam divididas em várias parcelas.

Uma compra poderá gerar diversas parcelas.

Cada parcela poderá possuir:

- Número da parcela;
- Quantidade total de parcelas;
- Valor;
- Data prevista;
- Data de pagamento;
- Situação;
- Fatura correspondente.

Isso permitirá consultar compromissos financeiros futuros e o total ainda pendente de pagamento.

### 🔄 Transações Recorrentes
Representação de receitas e despesas que acontecem periodicamente.

Exemplos:

- Salário;
- Aluguel;
- Netflix;
- Spotify;
- Internet;
- Mensalidades.

Deverão ser consideradas informações como periodicidade, valor, data inicial, data final e situação.

### 📈 Investimentos
Módulo destinado ao controle da carteira de investimentos.

O sistema poderá representar diferentes classes de ativos:

- Ações;
- Fundos;
- ETFs;
- Renda fixa;
- Criptomoedas;
- Outros ativos financeiros.

Também deverão ser registradas operações como:

- Compra;
- Venda;
- Aporte;
- Resgate;
- Rendimentos.

As operações poderão armazenar:

- Data;
- Quantidade;
- Preço unitário;
- Taxas;
- Valor total.

Esses dados deverão permitir consultas relacionadas à quantidade acumulada, custo, preço médio, ganhos, perdas e rentabilidade.

### 🎯 Orçamentos e Metas
O usuário poderá estabelecer limites de gastos por categoria e período.

Exemplo:

> Limite de R$ 400,00 para a categoria Lazer durante determinado mês.

O banco deverá permitir comparar:

- Valor planejado;
- Valor efetivamente gasto;
- Valor restante;
- Percentual utilizado.

---

## 🔎 Consultas que o banco deverá possibilitar

A implementação deverá demonstrar consultas SQL de diferentes níveis de complexidade, como:

- Consultar todas as contas de um usuário;
- Consultar o saldo das contas;
- Listar todas as transações de determinado período;
- Consultar receitas e despesas por mês;
- Identificar as categorias com maior volume de gastos;
- Calcular o total gasto por categoria;
- Consultar faturas abertas, pagas e atrasadas;
- Consultar compras parceladas;
- Calcular o valor total de parcelas futuras;
- Identificar os maiores gastos;
- Comparar orçamento planejado e gasto realizado;
- Calcular o percentual utilizado de um orçamento;
- Consultar investimentos por tipo de ativo;
- Calcular quantidade de ativos adquiridos;
- Consultar operações de compra e venda;
- Consolidar o patrimônio financeiro do usuário;
- Utilizar `JOIN` entre múltiplas tabelas;
- Utilizar `SUM`, `COUNT`, `AVG`, `MIN` e `MAX`;
- Utilizar `GROUP BY` e `HAVING`;
- Utilizar filtros por período;
- Utilizar subconsultas quando necessário.

---

## 🧩 Requisitos de Modelagem

O projeto deverá explorar os conceitos apresentados na disciplina, incluindo:

- Entidades fortes;
- Entidades fracas, quando aplicável;
- Entidades associativas;
- Generalização e especialização;
- Relacionamentos 1:1;
- Relacionamentos 1:N;
- Relacionamentos N:M;
- Relacionamentos binários;
- Relacionamentos ternários, quando justificáveis;
- Atributos simples;
- Atributos compostos;
- Atributos multivalorados, quando aplicáveis;
- Chaves primárias (`PK`);
- Chaves estrangeiras (`FK`);
- Chaves compostas;
- Integridade referencial;
- Normalização.

Os conceitos deverão ser utilizados de maneira coerente com as regras de negócio, evitando adicionar estruturas apenas para cumprir requisitos sem justificativa.

---

## 🗃️ Tecnologias

- **SGBD:** MySQL
- **Linguagem:** SQL
- **Controle de versão:** Git
- **Repositório:** GitHub

---

## 📁 Estrutura prevista do repositório

```text
laboratorio-banco-dados-sistema-financeiro/
│
├── README.md
│
├── sql/
│   └── banco_financeiro.sql
│
├── diagramas/
│   ├── der-conceitual.*
│   ├── modelo-logico.*
│   └── modelo-fisico.*
│
└── docs/
    └── especificacao.md
```

---

## 👥 Divisão do trabalho

| Integrante | Responsabilidade |
|---|---|
| **Felipe** | Descrição detalhada do tema |
| **Erik** | DER conceitual |
| **Fernando** | Modelagem lógica |
| **Franklee** | Modelagem física |
| **Gustavo** | Implementação do banco de dados |

### Gustavo — Implementação

Responsável por:

- Criar o banco de dados;
- Criar as tabelas;
- Definir PKs e FKs conforme os modelos;
- Criar restrições de integridade;
- Inserir dados de teste;
- Criar consultas `SELECT`;
- Criar comandos `UPDATE`;
- Demonstrar consultas com `JOIN`, agregações e agrupamentos;
- Garantir fidelidade entre o SQL e os diagramas;
- Organizar os scripts no repositório.

---

## 🔗 Relação entre as etapas

A implementação deverá seguir a sequência:

**DER Conceitual → Modelo Lógico → Modelo Físico → SQL**

O script SQL deverá refletir os modelos desenvolvidos pelos integrantes do grupo, mantendo consistência entre entidades, atributos, relacionamentos, chaves e restrições.

---

## 📚 Disciplina

**Laboratório de Banco de Dados**

**Tema:** Finanças — Sistema de Controle Financeiro

**SGBD:** MySQL
