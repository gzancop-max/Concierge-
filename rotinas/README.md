# Rotinas

Uma única tarefa agendada dispara o **pulso horário** (`pulso-horario.md`), 24h por dia. O próprio pulso decide qual rotina rodar pelo horário:

| Rotina | Arquivo | Quando (America/Sao_Paulo) |
|---|---|---|
| Pulso (sempre) | `pulso-horario.md` | toda hora |
| Briefing matinal | `briefing-matinal.md` | 1º pulso após 07:00 |
| Manejo dos agentes | `manejo-agentes.md` | 1º pulso após 08:00 e após 16:00 |
| Fechamento + autocrítica | `revisao-noturna.md` + `auto-aprimoramento.md` | 1º pulso após 21:00 |
| Revisão semanal | `revisao-semanal.md` | domingo, no fechamento |

## Regras comuns
- O pulso decide se fala com o Giuseppe (critérios no §4 do pulso). Sem nada útil: não fala.
- Sempre termina com diário atualizado, tarefas/painel atualizados se mudaram, commit + push.
