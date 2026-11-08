# Pulso horário — o coração do Concierge

Roda **toda hora, 24h por dia**. Em cada pulso o Concierge reavalia tudo e **decide sozinho** se vale a pena falar com o Giuseppe agora.

> **Enquanto o GitHub estiver fora:** siga também `comunicacao/protocolo-backup-drive.md` — no início do pulso, leia a pasta `Mensagens` e os STATUS mais recentes de cada agente no Drive (é por lá que o Concierge acompanha os agentes agora); no fim, backup do Concierge no Drive.

## 1. Situar-se (sempre, rápido)
1. `git pull` no `Concierge-`. Hora local (America/Sao_Paulo). Leia o diário de hoje — principalmente a seção `## Pulsos` — para não repetir trabalho nem avisos.
2. Determine o **modo** pelo horário e pelo que já foi feito hoje:
   | Modo | Quando | Extra deste pulso |
   |---|---|---|
   | **Madrugada** | 23:00–06:59 | Trabalho silencioso. Só notifica se for **urgente de verdade** (ver §4). |
   | **Briefing** | primeiro pulso a partir das 07:00 | `rotinas/briefing-matinal.md` (depois que os agentes já rodaram 06:36–06:47) |
   | **Manejo dos agentes** | primeiro pulso a partir das 08:00, e de novo a partir das 16:00 | `rotinas/manejo-agentes.md` |
   | **Fechamento** | primeiro pulso a partir das 21:00 | `rotinas/revisao-noturna.md` + `rotinas/auto-aprimoramento.md` (autocrítica diária) |
   | **Semanal** | domingo, junto do fechamento | `rotinas/revisao-semanal.md` |
   | **Normal** | qualquer outro pulso | só os passos 2–5 abaixo |

## 2. Varrer as fontes (o que mudou desde o último pulso)
Pule em silêncio o que estiver indisponível; registre no diário se uma fonte cair por mais de um dia.
- **Gmail** (só leitura): mensagens novas com prazo, cobrança, pedido de pessoa real, hospital, residência, CEP, família.
- **Google Drive**: arquivos novos/alterados relevantes (TCC, documentos).
- **Agenda**: compromissos das próximas 24 h (se o conector estiver disponível).
- **Agentes**: `last_run` das tarefas agendadas deles (ferramenta `list_triggers`) — falhou? atrasou?
- **Tarefas**: prazos de `tarefas/TAREFAS.md` vencendo.
- **Internet**: só quando algo concreto pedir (clima em dia de deslocamento, notícia que afeta um compromisso).

## 3. Agir (nível A/B sem perguntar)
Resolva o que puder antes de pensar em avisar: transformar e-mail em tarefa, preparar rascunho, pesquisar, atualizar painel, reorganizar tarefas.

## 4. Decidir: falar com o Giuseppe agora?
Fale **só** se pelo menos um for verdadeiro:
- 🔴 Algo exige ação dele **nas próximas horas** (prazo, compromisso, pedido urgente de pessoa real, falha que só ele resolve).
- 🟠 Uma decisão dele está **travando** um agente ou o Concierge, e esperar até o próximo briefing/fechamento custa caro.
- 🟢 É o pulso de briefing ou fechamento (contato esperado).
- 💡 Uma oportunidade **com prazo curto** e muito alinhada ao perfil (ex.: o Radar achou item da lista de desejos no preço-alvo).

**Não fale** se: é rotina, já foi avisado hoje (mesmo assunto), ele provavelmente está em plantão/cirurgia e não é 🔴, ou é madrugada e não é 🔴.
Limite: no máximo **4 contatos fora do briefing/fechamento por dia**. Junte assuntos quando puder.

Como falar: ferramenta `PushNotification` (até 200 caracteres, começando pelo que ele precisa fazer) **e** a mensagem final do pulso com o detalhe. Se não for falar, a mensagem final é uma linha: `Pulso HH:MM — sem contato (motivo curto).`

## 5. Registrar (sempre) — e, sem GitHub, backup no Drive conforme o protocolo
Acrescente ao `diario/AAAA-MM-DD.md`, em `## Pulsos`:
`- HH:MM — modo — o que vi — o que fiz — contatei? (sim/não + motivo)`
Atualize tarefas/painel se mudaram. Commit + push (`pulso: HH:MM ...`) **só se o pulso teve novidade**; pulso sem novidade só acrescenta a linha no diário, sem commit (ela entra no próximo commit). (ajuste de 07/11)

## Custo
Pulso normal deve ser leve (poucos minutos). Trabalho pesado vai para os pulsos de manejo/fechamento ou para os próprios agentes.
