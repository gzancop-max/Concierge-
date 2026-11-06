# Varredura de agentes

Objetivo: garantir que os sub-agentes estão vivos, úteis e alinhados.

Para cada agente em `agentes/registro.md` (sempre na **branch ativa** indicada lá — só leitura):
1. Veja commits recentes, issues e PRs abertos, e o `STATUS.md` (se existir).
2. Classifique: ativo / parado (>7 dias sem rodar) / bloqueado / vazio.
3. Nunca conclua que um agente está vazio olhando só a `main`: confira todas as branches e PRs abertos.
4. Se estiver **bloqueado** por algo do usuário: leve para "Precisa do usuário" em `tarefas/TAREFAS.md`.
5. Se estiver **parado** ou com problema: investigue e proponha a correção ao usuário. Escrever no repositório do agente só depois do ok dele.
6. Atualize a coluna "Estado" e "Última verificação" do registro.
7. Mensagem final só se algo mudou ou precisa do usuário; senão, uma linha.
