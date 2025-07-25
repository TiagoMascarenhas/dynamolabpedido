# Laboratório AWS - DynamoDB com LSI e GLI

Este repositório contém o laboratório prático realizado como parte da formação da Escola da Nuvem, com foco na utilização do serviço **DynamoDB** da AWS.

---

## 📌 Objetivo

Criar uma tabela no DynamoDB com os seguintes requisitos:

- Chave de partição: `ID do Usuário`
- Chave de ordenação: `Data do Pedido`
- Índice Secundário Local (LSI): `Status`
- Índice Secundário Global (GLI): `Status` + `ValorTotal`

E realizar operações de:

- Criação de tabela
- Inserção de itens manualmente e via terminal (CloudShell)
- Consultas otimizadas com uso de índices

---

## 🧪 O que foi praticado

- Criação de tabela no DynamoDB
- Diferença entre consultas simples, com filtros, com LSI e com GLI
- Importação de dados via CloudShell
- Uso do comando `batch-write-item`
- Análise de eficiência das queries
- Exclusão de índices e tabela para evitar cobrança

---

## ✅ Habilidades Demonstradas

- Configuração de infraestrutura na nuvem (AWS)
- Gerenciamento de segurança (alertas de orçamento)
- Uso de terminal AWS (CloudShell)

---

## ▶️ Como Reproduzir

1. Acesse a AWS Console e vá para o serviço **DynamoDB**
2. Crie a tabela com os atributos e índices indicados
3. Faça a inserção dos dados conforme instruções
4. Execute as consultas com e sem uso de índices
5. Ao final, exclua os recursos para evitar cobranças

---

## 🖼️ Prints

| Consulta via GLI 
(<img width="1197" height="724" alt="image" src="https://github.com/user-attachments/assets/c99cdee1-b9a6-4007-8d1e-c41769e17f84" />
 ![LSI](<img width="1420" height="735" alt="image" src="https://github.com/user-attachments/assets/b01b9a26-bb16-464b-9611-5f3d7aad816e" />


---


## 🧠 Aprendizados

Durante o laboratório foi possível entender a importância do uso correto de índices no DynamoDB e como eles impactam diretamente a performance de leitura. Também aprendi a automatizar importações via terminal e a interpretar mensagens de eficiência das consultas.

---

## 📬 Contato

- GitHub: [TiagoMascarenhas](https://github.com/TiagoMascarenhas)
- LinkedIn: [Tiago Mascarenhas](https://www.linkedin.com/in/tiagomascarenhass)

> Repositório criado como parte da formação na Escola da Nuvem - Turma DEV3

**Tiago Mascarenhas**  
Julho/2025
