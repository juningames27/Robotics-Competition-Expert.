# Robotics Competition Expert

**Skill de robótica competitiva para OpenAI Codex**, com foco em Arduino, ESP32 e programação embarcada confiável.

A proposta é orientar o agente a **analisar prioridades, modelar estados, testar falhas e verificar o código** antes de considerar uma estratégia pronta. Ela não substitui medições na arena nem altera a inteligência do modelo.

## Como usar

1. Abra **este repositório no Codex** (por clone ou integração com repositórios).
2. Inicie uma sessão do Codex no projeto.
3. Peça: `$robotics-competition-expert Analise a estratégia do meu robô de sumô antes de escrever o código.`
4. Informe placa, driver, motores, sensores, pinos, alimentação e regras reais da competição.
5. Exija relatório do que foi testado, do que foi apenas analisado e do que falta medir na arena.

O arquivo `AGENTS.md` orienta o trabalho no projeto; a Skill está em `.agents/skills/robotics-competition-expert/SKILL.md`.

## Especialidades

- **Robot Sumô:** segurança de borda, busca, ataque, recuperação e prioridades de eventos simultâneos.
- **Tug of War:** tração, torque, limites de corrente, controle robusto dos motores.
- **Seguidor de linha:** calibração, PID, saturação, anti-windup e recuperação.
- **Balloon Battle:** detecção, evasão e decisões respeitando as regras.
- **ESP32/Arduino:** código não bloqueante, tratamento de ruído e compatibilidade de bibliotecas.

## Referências incluídas

- [Guia de lógica de sumô](.agents/skills/robotics-competition-expert/references/sumo.md)
- [Guia de cabo de guerra](.agents/skills/robotics-competition-expert/references/tug-of-war.md)
- [Checklist de engenharia embarcada](.agents/skills/robotics-competition-expert/references/embedded-checklist.md)
- [Ficha de hardware para preencher](.agents/skills/robotics-competition-expert/references/hardware-profile.md)
- [Exemplos de pedidos ao Codex](PROMPTS.md)

## Avisos

Esta Skill contém **instruções para o agente**. Não compila, mede ou controla um robô automaticamente. Simulações e cálculos são apoio para testes reais.

**Nenhum mapa de pinos, tensão, especificação de motor ou resultado experimental foi presumido.** Preencha sua ficha de hardware antes de implementar um robô.

## Fonte

Estrutura baseada no padrão de Skills com `SKILL.md` e `AGENTS.md` do Codex. Consulte a [documentação da OpenAI](https://developers.openai.com/api/docs/guides/tools-skills).
