# Uso prudente do GitHub (vale para todos os agentes)

Criado em 09/11/2026, depois da suspensão da conta gzancop-max (06–09/11), a pedido do Giuseppe.

## O que se sabe
- **O GitHub não informou o motivo** da suspensão (o suporte só confirmou o chamado #4965719).
- **Não foi limite de requisições:** em 09/11 a conta usava 1 de 15.000 chamadas/hora da API (REST), 3 de 10.000 (GraphQL), 0 de 30 buscas/min.
- **11/11/2026:** o suporte do GitHub (chamado KV6YL4-PKXGV) respondeu: o sistema antiabuso marcou a conta para revisão manual; as restrições foram retiradas e a conta está liberada. Confirma a hipótese abaixo — as regras continuam valendo.
- Hipótese mais provável: **conta nova com muita atividade automática de uma vez** (4 sessões fazendo commits e pushes em paralelo, centenas de commits em poucas horas, app OAuth autorizado no meio). Sistemas antiabuso do GitHub olham padrão de comportamento, não só cota.

## Limites oficiais (para nunca chegar perto)
- API REST: 15.000 req/h nesta conta; GraphQL: 10.000 pontos/h; busca: 30/min (código: 10/min).
- Limites secundários: até 100 requisições simultâneas, 900 pontos/min na REST, **80 criações de conteúdo/min e 500/h** (issues, comentários, PRs).

## Regras
1. **Push:** no máximo **1 push por rodada**, no fim dela. Nunca mais de **~10 pushes/dia por repositório**. Nunca force-push.
2. **Commits:** um commit por entrega (não por arquivo). Autoajustes de uma rodada vão juntos num commit.
3. **Pulso sem novidade não gera commit** (vale para o Concierge).
4. **API (MCP/gh):** só o necessário; nada de polling em laço; no máximo ~100 chamadas por rodada.
5. **Escritas na API** (issues, comentários, PRs): no máximo 5 por rodada, com pelo menos 1 s entre elas.
6. **Nunca:** criar repositórios, gists, tokens ou autorizar apps novos sem o Giuseppe pedir.
7. **Erro 403/429 ou "secondary rate limit":** pare de usar o GitHub naquela rodada, use o plano B do Drive (`comunicacao/protocolo-backup-drive.md`), registre no STATUS. Push que falhar: 1 nova tentativa, depois Drive — sem insistir.
