# Plano inicial de validação

## Objetivo

Demonstrar, com evidências, que a célula virtual executa a sequência prevista e classifica as peças corretamente.

## Casos mínimos de teste

| ID | Cenário | Resultado esperado | Estado |
|---|---|---|---|
| T-001 | Inicialização normal | Sistema entra em estado seguro e pronto | Planejado |
| T-002 | Peça aprovada | Peça é detectada e enviada ao destino correto | Planejado |
| T-003 | Peça reprovada | Peça é detectada e enviada ao destino correto | Planejado |
| T-004 | Sensor sem sinal | Sistema não avança indevidamente | Planejado |
| T-005 | Parada ou falha | Atuadores assumem condição segura | Planejado |

## Evidências previstas

- captura ou vídeo da simulação;
- tabela com entrada, ação e resultado;
- versão da lógica usada no teste;
- observações sobre falhas e correções.

## Critério inicial de conclusão

Todos os testes obrigatórios deverão ter resultado aprovado e evidência associada. Os critérios serão refinados quando a arquitetura e as categorias de inspeção forem definidas.
