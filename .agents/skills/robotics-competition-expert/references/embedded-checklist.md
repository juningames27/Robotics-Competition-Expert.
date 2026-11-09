# Checklist de firmware embarcado

- [ ] Placa, core, driver, pinos e bibliotecas confirmados.
- [ ] Alimentação e níveis lógicos compatíveis; GND comum onde aplicável.
- [ ] Máquinas de estados com prioridade explícita.
- [ ] Nenhum `delay()` bloqueia decisões críticas.
- [ ] Saídas para os motores definidas em todos os estados.
- [ ] Estados de inicialização e perda de comunicação seguros.
- [ ] Ruído e leituras inconsistentes previstos.
- [ ] Timeouts e transbordamento de `millis()` considerados.
- [ ] APIs de PWM compatíveis com versão do core.
- [ ] Compilação executada, ou indisponibilidade explicitamente informada.
- [ ] Testes de bancada e arena com critérios observáveis listados.
- [ ] Resultados medidos separados de hipóteses ou estimativas.
