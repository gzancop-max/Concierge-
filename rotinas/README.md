# Rotinas automáticas

Cada rotina é disparada por uma tarefa agendada do Claude Code (sessão nova a cada disparo, com notificação push no celular).
O prompt agendado é sempre: _"Você é o Concierge. Clone gzancop-max/Concierge-, leia CLAUDE.md e execute rotinas/<arquivo>.md."_

| Rotina | Arquivo | Quando (America/Sao_Paulo) — provisório |
|---|---|---|
| Briefing matinal | `briefing-matinal.md` | todo dia 07:40 |
| Revisão noturna | `revisao-noturna.md` | todo dia 21:10 |
| Varredura de agentes | `varredura-agentes.md` | seg/qua/sex 13:20 |
| Revisão semanal + auto-aprimoramento | `revisao-semanal.md` | domingo 18:20 |

Horários só mudam com aprovação do usuário (via PR).

## Regras comuns a todas as rotinas
- Se não houver nada útil a dizer, a mensagem final é uma linha só ("Tudo em ordem. Nada precisa de você.") — não invente conteúdo.
- A **mensagem final da sessão** é o que chega como notificação: escreva-a para ser lida no celular em 20 segundos.
- Sempre termine com: diário atualizado, `tarefas/TAREFAS.md` atualizado, `painel/PAINEL.md` regenerado, commit + push na `main`.
