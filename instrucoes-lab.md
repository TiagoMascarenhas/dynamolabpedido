# Instruções do Laboratório - DynamoDB com LSI e GLI

Este documento contém um resumo passo a passo do laboratório realizado utilizando Amazon DynamoDB. Ele segue a proposta da Escola da Nuvem, focando na criação e manipulação de dados com uso de índices secundários locais e globais.

---

## ✅ Etapas do Laboratório

### 1. Criar Tabela DynamoDB
- Nome: `Pedido-tiago`
- Chave de partição: `ID do Usuário` (String)
- Chave de ordenação: `Data do Pedido` (String)

### 2. Configurações da Tabela
- Capacidade: provisionada (5 leitura / 5 gravação)
- Classe: DynamoDB Standard
- Desativar Auto Scaling

### 3. Criar Índice Secundário Local (LSI)
- Nome: `LSI-PedidotiagoStatus`
- Chave de classificação: `Status` (String)
- Projeção: All

### 4. Inserir Item Manualmente (via Console)
- `ID do Usuário`: U000
- `Data do Pedido`: 2025-05-16
- `Endereco` (mapa): bairro, cidade, estado, número, rua
- `tags` (lista): Ex: "Entrega zona rural", "Equipe Rocket", "Recife"
- `IDPedido`: P1000
- `Status`: Pendente
- `ValorTotal`: 900

### 5. Popular a Tabela via CloudShell
1. Fazer upload do arquivo `pedidos_import.json`
2. Executar:
   ```bash
   aws dynamodb batch-write-item --request-items file://pedidos_import.json
   ```

### 6. Consultas no Console
- **Consulta por Verificação**: Busca geral (menos eficiente)
- **Consulta por Chave Primária**: ID do usuário = `U001` (mais eficiente)

### 7. Consulta via LSI
- Selecionar índice `LSI-PedidotiagoStatus`
- Chave de partição: `ID do Usuário = U001`
- Chave de ordenação: `Status = Entregue`

### 8. Consulta com Filtro Adicional via LSI
- Mesmo índice
- Filtro adicional: `ValorTotal >= 80`

### 9. Criar Índice Secundário Global (GLI)
- Nome: `GLI-Status-ValorTotal`
- Chave de partição: `Status` (String)
- Chave de ordenação: `ValorTotal` (Number)

### 10. Consulta via GLI
- Status: `Entregue`
- ValorTotal: `>= 60`

---

## 🧹 Encerramento

### Excluir recursos criados para evitar cobranças:
1. Excluir índice GLI no console da AWS
2. Excluir a tabela principal

---

> Essas etapas cobrem desde a modelagem inicial até a execução e análise de consultas otimizadas usando os índices. O laboratório reforça o impacto da modelagem correta em performance de leitura no DynamoDB.

**Tiago Mascarenhas – Julho/2025**
