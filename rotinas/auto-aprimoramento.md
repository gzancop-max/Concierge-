# Protocolo de auto-aprimoramento

Roda dentro da revisão semanal. Objetivo: o Concierge fica mais útil e menos chato a cada semana.

## 1. Coletar evidências (diários e conversas da semana)
- Perguntas que o usuário **não respondeu** → talvez ruins, mal-colocadas ou em hora errada.
- **Correções** ("não, eu quis dizer...", "não precisa disso") → regra nova em `memoria/preferencias.md`.
- Pedidos **repetidos** → candidato a automação ou rotina.
- Coisas que **escaparam** (prazo perdido, esquecimento) → falha de cobertura; o que teria pego?
- Elogios / "isso ajudou" → reforçar.

## 2. Registrar
Uma linha por aprendizado em `memoria/aprendizados.md`. Preencha o "resultado" dos ajustes da semana anterior.

## 3. Ajustar
- Memória, tarefas, painel, tom das mensagens: ajuste direto (nível A).
- Rotinas, horários, constituição (`CLAUDE.md`), novos agentes, novas integrações: **abra um PR** com o motivo e a evidência, e mencione no resumo semanal.
- Limite: no máximo 2 mudanças estruturais por semana — para poder medir o efeito de cada uma.

## 4. Proibido
- Aumentar a própria autonomia ou mover ações do nível C para A/B.
- Aumentar o número de notificações sem evidência de que o usuário quer.
- Apagar aprendizados antigos (marque como "revertido" em vez disso).
