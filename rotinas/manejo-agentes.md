# Manejo diário dos agentes (2× por dia)

Os agentes rodam sozinhos e se auto-aprimoram. O Concierge **não substitui** isso: ele é o gerente que confere, cobra, conecta e corrige o rumo.

Para cada agente em `agentes/registro.md` (na branch ativa — só leitura):
1. **Rodou?** `list_triggers` → `last_run` de cada rotina do agente. Falhou ou não rodou no horário → investigue (eventos da sessão com `list_events`).
2. **Entregou?** Leia o relatório/registro do dia (TCC: `relatorios/` e `estado/projeto.json`; Radar: `relatorios/` e `docs/data/stats.json`; Papelada: `docs/CICLOS.md`, `docs/BACKLOG.md`). Houve produto concreto ou só movimento?
3. **Está no rumo?** Compare com os objetivos do Giuseppe (perfil) e com as prioridades do próprio agente. Ex.: a Papelada está simplificando ou acrescentando telas? O TCC está atacando o maior risco para a defesa?
4. **Precisa do Giuseppe?** Junte as pendências de cada agente num só lugar (`tarefas/TAREFAS.md` → "Precisa do usuário"), sem duplicar, com a resposta sugerida.
5. **Conectar agentes:** algo que um sabe e outro precisa (ex.: dado correto do CRM, data da defesa, plantões que mudam horários).
6. **Avaliar o auto-aprimoramento deles:** as mudanças que fizeram em si mesmos ajudaram? Alguma regra perigosa foi afrouxada?

## O que o Concierge pode fazer
| Ação | Nível |
|---|---|
| Ler repositórios, relatórios, sessões, status das rotinas | A |
| Pedir para a sessão do agente refazer uma rodada que falhou (`send_message` na sessão dele) | B — faça e conte no próximo contato |
| Propor melhoria no agente (instruções, scripts, rotina) | C — descreva ao Giuseppe: repositório, o que muda e por quê; só depois do ok escreva (via PR) |
| Qualquer escrita em repositório de agente, issue, comentário, merge | C |

Registre o resultado em `agentes/registro.md` (estado + última verificação) e no diário.
