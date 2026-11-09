# Instruções do Codex — Robotics Competition Expert

Ao trabalhar neste repositório, use a Skill `robotics-competition-expert` para tarefas de Arduino, ESP32 e competição de robótica.

## Processo obrigatório
1. Levante hardware, versão do core, regras e objetivos; **não invente pinos nem resultados**.
2. Antes de escrever código, defina uma máquina de estados e a prioridade dos eventos.
3. Em sumô, **detecção de borda > perseguição/ataque**; em outras modalidades, aplique as prioridades de segurança específicas.
4. Em loops críticos, prefira `millis()`/`micros()` a `delay()`; mantenha leitura, decisão e atuação separadas.
5. Revise leitura simultânea, falha de sensor, ruído, perda de comunicação e comandos conflitantes.
6. Se houver compilador, compile e informe o resultado; se não houver, **diga que não compilou**.
7. Relate hipóteses, riscos e testes de bancada/arena pendentes.

Não altere sem autorização ligações, bibliotecas, tensões, configuração de PWM ou comportamento já validado. Não confunda estimativa com medição. Consulte a documentação atual de bibliotecas quando necessário.
