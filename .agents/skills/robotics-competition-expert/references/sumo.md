# Robot Sumô — prioridades e cenários

## Prioridade base
1. **Borda:** nunca iniciar/permanecer em ataque se o sensor indica saída iminente.
2. **Recuperação:** recuar e girar de modo a voltar ao interior da arena.
3. **Alvo presente:** atacar com direção/velocidade coerentes.
4. **Alvo perdido:** buscar e reacquirir adversário.
5. **Leituras inválidas:** parar ou usar estratégia segura validada em arena.

## Exemplo de máquina de estados
| Estado | Evento | Próximo estado | Ação |
| --- | --- | --- | --- |
| BUSCA | Borda | RECUO | Parar avanço, recuar |
| BUSCA | Alvo válido | ATAQUE | Avançar controladamente |
| ATAQUE | Borda | RECUO | Priorizar saída da borda |
| ATAQUE | Perda do alvo | BUSCA | Retomar busca |
| RECUO | Recuo concluído | GIRO | Girar para dentro da arena |
| GIRO | Giro concluído e sem borda | BUSCA | Retomar busca |

Parâmetros de recuo/giro devem ser calibrados fisicamente para o robô e a arena. Não invente tempos.

## Testes de arena
- Acionar alvo e borda simultaneamente: confirmar que borda vence.
- Acionar só cada sensor de borda, em ambos os lados.
- Testar perda do alvo durante avanço.
- Verificar sob ruído, velocidades diferentes e bateria parcialmente descarregada.
- Medir tempo de leitura, resposta e distância de frenagem.

Não presuma modelo de arena, sensores ou posição dos motores.
