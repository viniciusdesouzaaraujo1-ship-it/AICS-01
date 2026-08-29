# Descrição funcional da célula

## Decisão de projeto

O AICS-01 será uma célula virtual de inspeção e classificação de caixas por altura.

## Objetivo do processo

Transportar caixas por uma esteira, identificar caixas com altura fora do padrão e separar automaticamente as peças aprovadas das reprovadas.

## Categorias

- **Aprovada:** caixa de altura normal.
- **Reprovada:** caixa alta.
- **Falha de processo:** sinais incoerentes, caixa presa ou tempo de percurso excedido.

## Sequência automática

1. O operador comanda a partida.
2. Se as condições de segurança estiverem atendidas, a esteira é acionada.
3. O sensor de entrada detecta a chegada de uma caixa.
4. A caixa passa pelo ponto de inspeção.
5. O sensor de altura determina a classificação:
   - sem detecção no sensor alto: caixa aprovada;
   - com detecção no sensor alto: caixa reprovada.
6. A caixa aprovada continua até a saída normal.
7. A caixa reprovada é acompanhada até a posição de rejeição.
8. O empurrador avança, desvia a caixa e retorna.
9. O contador correspondente é incrementado.
10. O sistema fica pronto para a próxima caixa.

## Modos previstos

### Parado

Esteira e empurrador permanecem em condição segura.

### Automático

A célula executa continuamente a sequência de detecção, inspeção e classificação.

### Falha

O movimento é interrompido e o motivo da falha deve ser indicado. O retorno ao modo automático exige eliminação da causa e comando de rearme.

## Condições de segurança

- parada de emergência tem prioridade sobre os demais comandos;
- o empurrador só pode avançar quando a caixa reprovada estiver na posição correta;
- a esteira não deve reiniciar automaticamente após uma parada de emergência;
- sinais impossíveis ou tempo de percurso excessivo devem gerar falha;
- na inicialização, o empurrador deve estar recolhido.

## Premissas da primeira versão

- uma caixa será processada por vez;
- existirão apenas duas alturas de caixa;
- a classificação será feita por sensores digitais;
- os tempos máximos serão definidos durante os primeiros testes;
- a implementação inicial será totalmente virtual.
