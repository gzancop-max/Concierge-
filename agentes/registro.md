# Registro de sub-agentes

O Concierge coordena estes agentes. Cada um vive no próprio repositório.

| Agente | Repositório | Propósito | Estado | Última verificação |
|---|---|---|---|---|
| Concierge (este) | `gzancop-max/Concierge-` | Assistente pessoal e coordenador | ativo | 2026-11-06 |
| Agente de Promoções | `gzancop-max/Claude--agente-de-promo-es-` | Encontrar promoções/ofertas relevantes para o usuário (?) | vazio — só README | 2026-11-06 |
| Papelada Médica | `gzancop-max/Papelada-m-dica-` | Organizar/gerar documentação médica (?) | vazio — só README | 2026-11-06 |
| TCC | `gzancop-max/Claude-TCC` | Apoiar o trabalho de conclusão de curso (?) | vazio — só README | 2026-11-06 |

Propósitos com `(?)` são inferidos pelo nome — confirmar com o usuário.

## Contrato padrão de um sub-agente
Quando um agente for construído, o Concierge propõe (via PR no repositório dele) que tenha:
1. `CLAUDE.md` — instruções do agente, incluindo "reportar ao Concierge".
2. `STATUS.md` — atualizado pelo próprio agente ao fim de cada rodada:
   ```
   estado: ativo | parado | bloqueado
   ultima_rodada: AAAA-MM-DD
   feito: ...
   proximo: ...
   precisa_do_usuario: ... (ou "nada")
   ```
3. Issues com o rótulo `concierge` para trabalho delegado pelo Concierge.

## Como delegar
- **Tarefa pontual**: abrir issue no repositório do agente com rótulo `concierge`, critério de pronto claro.
- **Tarefa grande**: abrir uma sessão do Claude Code dedicada no repositório do agente, com o contexto necessário.
- **Acompanhar**: na varredura (`rotinas/varredura-agentes.md`), ler `STATUS.md`, issues e PRs abertos.

## Ideias de novos agentes (propor ao usuário, não criar sozinho)
- Finanças pessoais (contas a pagar, gastos, assinaturas).
- Saúde e hábitos (sono, exercício, consultas, exames).
- Casa e burocracias (documentos, renovações, manutenção).
