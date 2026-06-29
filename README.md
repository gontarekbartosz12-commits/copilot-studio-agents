# Microsoft Copilot Studio — AI Agents (Portfolio)

A set of conversational AI agents I designed and built in **Microsoft Copilot Studio** and the **Power Platform**, across five business domains. This repo documents each agent's purpose and configuration (instructions, knowledge / RAG, starter prompts) and how the agents export for source control / ALM.

> Built by **Bartosz Gontarek** — AI-First Developer & Automation Builder · https://stronevo.pl

## Why
I build AI agents and automations day to day (n8n, Claude Code, MCP). These Copilot Studio agents show the same skill set in Microsoft's no-code / low-code agent ecosystem: instruction design, knowledge grounding (RAG), conversation design, starter prompts and actions.

## Agents

| # | Agent | Domain | What it does |
|---|-------|--------|--------------|
| 1 | STRONEVO Support | Support / RAG | Answers questions about a web studio's services, grounded in the company website |
| 2 | Asystent Leadów STRONEVO | Sales / lead intake | Walks a prospect through project type, scope, budget & contact, then outputs a structured lead |
| 3 | Asystent Obsługi Klienta Amovo | E-commerce | Product, delivery, payment & returns help for an online store |
| 4 | Asystent Rekrutacyjny | HR | Pre-screens candidates (role, experience, skills, availability) into a fit summary |
| 5 | Agent IT Helpdesk | IT support | Triages common tickets (password reset, VPN, access, email, printers) step by step |

## How each agent is built
- **Instructions** — a clear system prompt: role, tasks, tone, guardrails.
- **Knowledge / RAG** — grounding sources (e.g. a website) plus a say-you-don't-know fallback.
- **Starter prompts** — suggested opening questions.
- **Topics & actions** — conversation flows; full-maker agents can call Power Automate flows / APIs.

### 1 · STRONEVO Support
Polish-speaking support assistant for the STRONEVO web studio. Explains services (websites, landing pages, WooCommerce/Shopify stores, care & hosting, SEO, AI automation), the workflow (quote → design → build → launch) and timelines; answers grounded in stronevo.pl; collects name/e-mail/project for a quote.
Knowledge: stronevo.pl · Starter prompts: Oferta / Wycena / Czas realizacji

### 2 · Asystent Leadów STRONEVO
Conversational lead-intake agent: asks about project type (website / store / landing), scope & features, budget and contact, then summarises everything as a ready lead for the team.

### 3 · Asystent Obsługi Klienta Amovo
Customer-service agent for the Amovo online store: products, availability, InPost delivery, payments, shipping times, returns & complaints (14-day right of withdrawal); helps place an order.

### 4 · Asystent Rekrutacyjny
Candidate pre-screening agent: asks about target role, years of experience, key skills/technologies, availability and salary expectations, then summarises the candidate profile with a first fit assessment.

### 5 · Agent IT Helpdesk
Internal IT helpdesk agent: handles common employee tickets (password reset, login/VPN, app access, email setup, printers), diagnoses step by step, and when it cannot resolve, produces a concise ticket summary (category, description, urgency) for the IT team.

## Export & ALM
Full Copilot Studio agents are packaged in a Power Platform solution and exported as an unmanaged .zip (Solutions → Export → Unmanaged → Download), then unpacked with the Power Platform CLI (pac solution unpack) into source files for version control. Solution exports are added here as they are produced.

## Tech
Microsoft Copilot Studio · Power Platform · Power Automate · RAG / knowledge grounding · conversational design · prompt engineering

## License
See LICENSE. © 2026 Bartosz Gontarek — published for portfolio & educational purposes.
