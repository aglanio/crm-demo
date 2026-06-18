# OmniLead — CRM White-label com SDR de IA (Demo navegável)

CRM de leads para qualquer negócio que recebe contatos por vários canais e perde venda por **demora na 1ª resposta** e **follow-up manual inconsistente**.

No centro: a **Sofia**, um SDR de IA que responde em menos de 1 minuto em qualquer canal, qualifica o lead, envia as informações certas e **agenda a call do closer humano** — que passa a focar só em fechar.

Este repositório é um **protótipo de interface 100% front-end, sem build e sem dependências**. Todos os dados são fictícios (mock) — feito para **validação de fluxo, apresentação comercial e ponto de partida de UI**.

## Telas inclusas

- 📊 **Dashboard** — KPIs de funil, ranking de closers, tempo de 1ª resposta e gráficos
- 🗂️ **Pipeline / Kanban** — Interessado → Agendado → Escalado → Cliente ativo → Resolvido, com envelhecimento automático de leads frios
- 💬 **Atendimento multicanal** — WhatsApp (oficial Meta + QR), Instagram, e-mail, SMS e voz IA
- 🤖 **SDR de IA (Sofia)** — responde, qualifica, agenda e faz handoff pro humano
- 📞 **Score de call** — nota + insights da ligação como feedback pro closer
- 📣 **Campanhas** — e-mail, WhatsApp e SMS com métricas (enviados/abertos/cliques)
- ✅ **Templates WhatsApp HSM** — fluxo de aprovação Meta (approved/pending/rejected)
- ⚙️ **Automações + construtor de fluxos** — gatilhos de resposta, qualificação, follow-up T+4h/T+12h, NPS D+7
- 💰 **Faixas de orçamento / pacotes** configuráveis

## Rodar local

```bash
# qualquer servidor estático, ex:
python -m http.server 8000
# abre http://localhost:8000
```

Ou apenas abra `index.html` no navegador.

## Stack

- HTML estático
- [Tailwind CSS](https://tailwindcss.com) (CDN)
- [Chart.js](https://www.chartjs.org) (CDN)

Sem backend, sem npm, sem build.

> ⚠️ **Demo de interface** — dados fictícios, sem integrações reais (WhatsApp / IA / e-mail são simulados). Pensado para demonstração e prototipagem de UI.

## Licença

Proprietário — uso interno / demonstração.
