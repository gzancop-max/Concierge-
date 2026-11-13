# Registro de sub-agentes

O Concierge coordena estes agentes. **Leitura livre; escrita só com aviso prévio ao usuário** (ver `CLAUDE.md`).

> **Manejo 11/11 08:20:** TCC e Radar rodaram e entregaram (TCC: shell de Resultados; Radar: painel v15). Papelada sem rotina. Sessões longas com custo alto acumulado — avaliar no semanal.

> **GitHub voltou em 09/11** (antes: suspenso 06–09/11; o Drive segue como plano B). Acompanhe os agentes pelo Drive — STATUS na pasta de cada um e a pasta `Mensagens` (IDs em `comunicacao/protocolo-backup-drive.md`). O prompt que o Giuseppe colou nos agentes está em `comunicacao/prompt-para-agentes.md`.

> Atenção (06/11/2026): o trabalho dos três agentes está em **branches com PR #1 em rascunho, ainda não mesclado**. A `main` deles só tem o README. Até o merge, leia sempre a branch ativa abaixo.

| Agente | Repositório | Branch ativa | Propósito | Rotinas agendadas (SP) | Painel |
|---|---|---|---|---|---|
| **Agente TCC** | `gzancop-max/Claude-TCC` | `claude/tcc-admin-agent-8j5fzu` (PR #1) | Administra e faz andar o TCC: Plataforma Brasil/CEP, Gmail, literatura, análise em R, revisões do texto | 06:47 rotina completa · 15:17 bloco · 20:37 bloco + autoavaliação | https://claude.ai/artifact/MUs7hWKEnEVW8sBVbjX2MU |
| **Radar de Oportunidades** (promoções) | `gzancop-max/Claude--agente-de-promo-es-` | `claude/sweet-clarke-c0047y` (PR #1) | Caça ofertas verificadas (hardware, jogos, medicina, casa, ferramentas, viagens, benefícios) com batedores e verificador | 06:36 caçada diária | https://claude.ai/artifact/Wb7zyN4g2xyA6RNhiXHbQf |
| **Papelada Cirúrgica** (Gerente) | `gzancop-max/Papelada-m-dica-` | `claude/hopeful-heisenberg-klqrlv` (PR #1); base v2 em `legado/v2` ; **PR #2** `claude/busy-dirac-oygibz` (MCP do Conecte/Wareline, 12/11) | App HTML offline + Apps Script que gera evoluções, ambulatório, plantão, descrição cirúrgica/alta. Prioridade nº 1: **simplificar** | nenhuma encontrada (roda por ciclos `/ciclo`) | — |
| Triagem do e-mail (rotina avulsa) | — | — | Triagem matinal do Gmail + rascunhos de resposta (nunca envia) | 06:45 seg–sex | — |

## O que cada agente precisa do usuário hoje (lido em 06/11/2026)
- **TCC:** confirmar com a COREME a data exata da defesa; decisões de método e pontos da versão revisada do TCC (ver painel do TCC).
- **Papelada:** percorrer os 7 roteiros da v2, cadastrar equipes por hospital, confirmar diluições das drogas da UTI, revisar decisões autônomas (`docs/PENDENCIAS_USUARIO.md`).
- **Promoções:** preencher a lista de desejos real (hoje só tem exemplos) e votar no painel.

## Inconsistências encontradas (para propor correção — com aviso antes)
1. **CRM divergente:** o agente TCC registra o CRM correto como 238339 (SP); o `CLAUDE.md` da Papelada usa 238449 (o número errado). Se a Papelada imprime o CRM em documentos, sai errado.
2. **E-mail:** o agente TCC envia avisos por e-mail ao usuário. O usuário disse ao Concierge que não quer comunicação por e-mail — confirmar se a regra vale para os outros agentes também (o Radar já desligou o e-mail).
3. **Três PRs em rascunho não mesclados:** sessões novas abrem a `main` vazia; as rotinas atuais funcionam porque usam a branch, mas é frágil.

## Contrato sugerido para cada agente (propor, não impor)
- `STATUS.md` atualizado ao fim de cada rodada: `estado`, `ultima_rodada`, `feito`, `proximo`, `precisa_do_usuario`.
- Hoje o Concierge consegue ler o equivalente em: TCC → `estado/projeto.json` + `relatorios/`; Radar → `relatorios/` + `docs/data/stats.json`; Papelada → `docs/CICLOS.md`, `docs/BACKLOG.md`, `docs/PENDENCIAS_USUARIO.md`.

## Ideias de novos agentes (propor ao usuário, não criar sozinho)
- Transição de residente para especialista: título, prova, congressos, CNPJ/contabilidade, finanças.
- Saúde e descanso: escala de plantões, sono, exercício.
- Casa e burocracias: documentos, renovações (inclusive passaporte italiano/UE), manutenção.
