# Canais de comunicação

**Regra fixa: nunca e-mail.**

## Fase 1 — já funciona, sem configurar nada
- **Claude app no celular (notificações push).** Cada rotina agendada termina com uma mensagem curta que chega como notificação. O usuário responde abrindo a sessão — ali mesmo é a conversa.
- **Painel** em `painel/PAINEL.md` — legível no app do GitHub ou no navegador.
- **Conversa direta**: abrir uma sessão do Claude Code no repositório `Concierge-` e falar normalmente (texto ou voz no app).

## Fase 2 — mensageiro (decisão do usuário)
| Opção | Prós | Contras | Esforço |
|---|---|---|---|
| **Telegram bot** (recomendado) | Grátis, API aberta, configura em 10 min pelo @BotFather, aceita voz/foto/arquivo | Precisa usar o Telegram | Baixo |
| **WhatsApp (Meta Cloud API)** | O app que você já usa | Exige conta Meta Business, número dedicado, templates aprovados para mensagens proativas; custo por conversa | Alto |
| **WhatsApp via Twilio** | Mais simples que a Meta direta | Pago, sandbox limitado; produção também exige aprovação | Médio |

Arquitetura da Fase 2 (quando aprovada): um pequeno serviço (ex.: Cloudflare Worker ou Fly.io) recebe as mensagens do bot, grava como tarefa/issue no repositório `Concierge-` e dispara uma sessão do Concierge; as rotinas passam a enviar o resumo também pelo bot. Tokens ficam como segredos do ambiente — nunca no repositório.
