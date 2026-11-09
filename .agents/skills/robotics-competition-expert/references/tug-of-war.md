# Tug of War — engenharia de tração

## Objetivos
- **Maximizar força útil de tração** dentro das regras, evitando quedas de tensão e aquecimento.
- Dimensionar redução, raio da roda, aderência, corrente de partida e limites do driver.
- Separar condições mecânicas de falhas de lógica.

## Estimativas úteis
- Força de tração ideal na periferia da roda: `F = torque_na_roda / raio`.
- Limite por aderência: `F <= mu * N` (modelo simplificado; depende da distribuição de peso).
- Corrente em travamento e capacidade da bateria, driver e cabos devem ser verificadas em datasheets e testes controlados.
- Números calculados são apenas estimativas: comparar com testes reais.

## Regras de código
- Definir partida segura e proteção contra perda de comando.
- Não aumentar PWM cegamente quando o motor está travado.
- Evitar mudanças bruscas de direção sob carga sem justificativa e verificação.
- Não mudar pinos de ponte H informados nem supor que ENA/ENB usem PWM válido.

## Testes
- Medir tensão sob carga, corrente e aquecimento (com instrumentos adequados).
- Repetir tração com superfície e peso conhecidos.
- Comparar curvas de aceleração e estratégias sob mesmo critério.
