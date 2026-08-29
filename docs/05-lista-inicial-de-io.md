# Lista inicial de entradas e saídas

Esta lista define os sinais lógicos mínimos da primeira versão. Os endereços definitivos serão atribuídos quando a plataforma de controle for escolhida.

## Entradas digitais

| Tag | Dispositivo | Função | Estado ativo |
|---|---|---|---|
| `PB_START` | Botão de partida | Solicita início do modo automático | Pressionado |
| `PB_STOP` | Botão de parada | Solicita parada normal | Pressionado |
| `PB_RESET` | Botão de rearme | Limpa falha após eliminar a causa | Pressionado |
| `ESTOP_OK` | Emergência | Indica circuito de emergência liberado | Ligado |
| `S_ENTRY` | Sensor de entrada | Detecta chegada de uma caixa | Caixa presente |
| `S_HEIGHT` | Sensor superior | Detecta caixa alta | Caixa alta presente |
| `S_REJECT_POS` | Sensor de rejeição | Confirma caixa diante do empurrador | Caixa presente |
| `S_EXIT_OK` | Sensor de saída | Confirma saída de caixa aprovada | Caixa presente |
| `S_PUSHER_RET` | Fim de curso | Confirma empurrador recolhido | Recolhido |
| `S_PUSHER_EXT` | Fim de curso | Confirma empurrador avançado | Avançado |

## Saídas digitais

| Tag | Atuador ou indicação | Função | Estado ativo |
|---|---|---|---|
| `M_CONVEYOR` | Motor da esteira | Movimenta as caixas | Esteira ligada |
| `Y_PUSHER_EXT` | Válvula do empurrador | Avança o empurrador | Energizada |
| `Y_PUSHER_RET` | Válvula do empurrador | Recolhe o empurrador | Energizada |
| `H_RUN` | Indicador verde | Indica modo automático | Ligado |
| `H_FAULT` | Indicador vermelho | Indica falha ativa | Ligado |

## Variáveis internas

| Tag | Tipo sugerido | Função |
|---|---|---|
| `AUTO_ACTIVE` | Booleano | Memória do modo automático |
| `BOX_REJECT` | Booleano | Memória de classificação da caixa atual |
| `FAULT_ACTIVE` | Booleano | Indicação geral de falha |
| `COUNT_OK` | Inteiro | Total de caixas aprovadas |
| `COUNT_NOK` | Inteiro | Total de caixas reprovadas |
| `T_TRAVEL` | Temporizador | Supervisiona o deslocamento da caixa |
| `T_PUSHER` | Temporizador | Supervisiona o ciclo do empurrador |

## Observação sobre implementação

A lista poderá ser reduzida durante o primeiro protótipo no Factory I/O. Os fins de curso e indicadores devem ser mantidos na especificação mesmo que a cena inicial ainda não os utilize, pois serão importantes para a validação completa.
