# PRD — CRM Demo (CRM de Leads para Espaços de Eventos)

> Documento de produto do protótipo. Define **o quê** o produto entrega e **por quê**.
> O artefato neste repositório é um **protótipo front-end navegável** (mock, sem backend) usado para validação de fluxo e apresentação comercial.

---

## 1. Visão

CRM vertical para **espaços e buffets de eventos** (casamentos, confraternizações, degustações) que recebem muitos leads por múltiplos canais e perdem vendas por **demora na primeira resposta** e **follow-up manual inconsistente**.

A proposta: um **SDR de IA** ("Sofia") que responde em < 1 min em qualquer canal, qualifica o lead (data + nº de convidados + orçamento), envia faixas de orçamento e **agenda a call do closer humano** — que passa a focar só em fechar.

## 2. Problema

- Lead de evento é de **alto ticket** (R$ 28k–90k) e **baixo volume** → cada lead perdido dói.
- Chega por muitos canais ao mesmo tempo: Instagram, Google, WhatsApp, Meta Ads, ligação.
- Resposta humana demora minutos/horas; o lead já falou com 3 concorrentes.
- Follow-up depende de memória do vendedor → leads esfriam sem ninguém perceber.
- Risco operacional no WhatsApp: disparo fora da janela de 24h sem template oficial = bloqueio.

## 3. Persona

| Persona | Dor | O que o produto entrega |
|---|---|---|
| **Dono(a) do espaço** | Vê faturamento vazar por lead mal atendido | Visibilidade do funil + IA que não dorme |
| **Closer / comercial** | Atola em atendimento repetitivo, sobra pouco pra fechar | Recebe só lead qualificado, com contexto e score da call |
| **Lead (noivo/cliente)** | Quer resposta rápida e orçamento claro | Atendimento imediato 24/7 + 3 faixas de orçamento |

## 4. Objetivos & métricas de sucesso

| Objetivo | Métrica | Alvo |
|---|---|---|
| Responder rápido | Tempo da 1ª resposta | < 1 min (IA) |
| Qualificar sem humano | % leads qualificados pela IA | ≥ 70% |
| Liberar o closer | % do tempo do closer em fechamento | 70–80% |
| Não perder lead frio | Reativação automática > 30d | Fluxo ativo |
| Segurança WhatsApp | Disparos fora de 24h só via template Meta | 100% |

## 5. Escopo do protótipo (features navegáveis hoje)

- **Dashboard** — KPIs de funil, ranking de closers, tempo de 1ª resposta, gráficos.
- **Pipeline / Kanban** — etapas: Interessado → Agendado → Escalado (IA sem resposta / pediu humano) → Cliente ativo → Resolvido. Envelhecimento automático de leads inativos.
- **Atendimento multicanal** — WhatsApp (oficial Meta + não-oficial QR), Instagram, e-mail, SMS, voz IA.
- **SDR de IA (Sofia)** — responde, qualifica, envia orçamentos, agenda call, faz handoff pro humano.
- **Score de call** — IA analisa a ligação e devolve nota + insights + feedback pro closer.
- **Campanhas** — e-mail marketing + WhatsApp + SMS, com métricas (enviados/abertos/cliques).
- **Templates WhatsApp Oficial (HSM)** — fluxo de aprovação Meta (approved/pending/rejected) com motivo.
- **Automações** — gatilhos de resposta imediata, qualificação, envio de orçamento, follow-up T+4h/T+12h, handoff, NPS pós-venda D+7.
- **Construtor de fluxos** — editor visual de sequências por gatilho.
- **Faixas de orçamento** — pacotes configuráveis (Essencial / Premium / Exclusivo).
- **Conexões de canais** — múltiplos números WhatsApp (oficial + não-oficiais) simultâneos.

## 6. Regra de canal (crítica)

- **Dentro de 24h** (cliente falou por último): WhatsApp livre.
- **Fora de 24h**: reabrir só com **template oficial Meta aprovado**.
- **Follow-up de lead sumido**: sai por **e-mail e SMS** — nunca WhatsApp não-oficial (risco de bloqueio).
- **Ligação humana** é o último passo do funil.

## 7. Fluxo principal (happy path)

```
Lead chega (qualquer canal)
  → IA responde < 1min
  → IA qualifica (data + convidados + orçamento)
  → IA envia 3 faixas de orçamento
  → Lead aceita → IA agenda call na agenda do closer (handoff)
  → Closer valida fit na call → marca degustação presencial
  → Degustação aprovada → contrato + onboarding pós-venda
  → D+7 pós-evento → NPS + pedido de indicação
```

Caminho de exceção: sem resposta > 24h **ou** "quero falar com alguém" → cria tarefa pro closer com contexto completo + notificação.

## 8. Fora de escopo (protótipo)

- Backend, persistência real, autenticação — **tudo é mock client-side**.
- Integrações reais com provedores de WhatsApp/e-mail/SMS/voz.
- Multi-tenant / cobrança / billing.
- App mobile nativo.

## 9. Roadmap (fases indicadas no produto)

| Fase | Entrega |
|---|---|
| **1 — atual** | Funil + atendimento multicanal + SDR IA + campanhas (protótipo navegável) |
| **2** | Backend real, integrações de canal, multi-tenant, auth |
| **3** | **Voz IA** ativa (atendimento e follow-up por ligação) |

## 10. Requisitos técnicos (protótipo)

- Front-end estático: HTML + Tailwind (CDN) + Chart.js (CDN). Sem build, sem dependências.
- Roda em qualquer servidor estático ou abrindo `index.html`.
- Todos os dados são fictícios, para demonstração.

---

_Protótipo de demonstração. Não contém dados reais de clientes nem infraestrutura de produção._
