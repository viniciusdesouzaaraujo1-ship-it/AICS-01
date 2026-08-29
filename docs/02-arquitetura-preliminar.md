# Arquitetura preliminar

## Visão funcional

Fluxo inicial proposto:

```text
Peça → Detecção → Inspeção → Decisão → Classificação → Registro do resultado
```

## Blocos técnicos previstos

- **Factory I/O:** representação da célula, sensores, atuadores e movimentação.
- **TIA Portal / S7-PLCSIM:** lógica do PLC e controle da sequência, caso a instalação seja viabilizada.
- **Wokwi / ESP32:** estudo de sistemas embarcados e protótipos de sinais ou comunicação.
- **CAD:** criação ou adaptação de peças e componentes mecânicos.
- **Excel:** tabela de testes, resultados e indicadores.
- **GitHub:** versionamento, documentação e evidências do progresso.

## Interfaces a definir

- lista e endereçamento de entradas e saídas;
- protocolo de comunicação entre ferramentas;
- estados operacionais e condições de falha;
- formato dos registros de teste.

Esta arquitetura é preliminar e deverá ser atualizada após a definição dos requisitos funcionais.
