# DynamoDB - Laboratório com LSI e GLI

Repositório criado para documentar o laboratório prático realizado como parte dos estudos com a Escola da Nuvem. O objetivo foi aplicar conceitos de bancos de dados NoSQL utilizando o serviço Amazon DynamoDB, com foco na criação e uso de índices secundários locais (LSI) e globais (GLI).

---

## 🚀 Objetivo do Projeto

- Criar uma tabela no DynamoDB com:
  - Chave de partição: `ID do Usuário`
  - Chave de ordenação: `Data do Pedido`
- Adicionar um índice secundário local (LSI) com a chave `Status`
- Adicionar um índice secundário global (GLI) com `Status` e `ValorTotal`
- Popular a tabela com dados manualmente e via terminal CloudShell
- Realizar consultas usando as diferentes formas disponíveis

---

## 🛠️ Tecnologias Utilizadas

- **AWS DynamoDB** – Serviço NoSQL da Amazon Web Services
- **AWS CloudShell** – Terminal nativo da AWS para automação
- **JSON** – Utilizado na importação em lote dos dados

---

## 📁 Estrutura do Repositório

```
dynamodb-lab-pedidotiago/
│
├── README.md                  # Este arquivo de explicação do projeto
├── pedidos_import.json        # Dados em lote para popular a tabela via terminal
├── imagens/                   # Prints das consultas realizadas no console da AWS
│   ├── consulta-gli.png
│   └── consulta-lsi.png
└── instrucoes-lab.md          # Resumo passo a passo do laboratório realizado
```

---

## 🔎 Exemplos de Consultas Realizadas

- Consulta simples por ID do usuário
- Consulta usando LSI: filtro por `Status` para determinado usuário
- Consulta usando GLI: busca por `Status` e pedidos com `ValorTotal` maior ou igual a determinado valor

Essas consultas foram fundamentais para observar como o uso correto de índices pode melhorar (ou piorar) a eficiência das operações de leitura no DynamoDB.

---

## 📌 Observações Finais

> Este repositório serve como documentação pessoal e também como referência prática para quem está aprendendo sobre bancos NoSQL com a AWS. Foi desenvolvido como parte do conteúdo da turma DEV3 da Escola da Nuvem.

---

**Tiago Mascarenhas**

Julho de 2025
