# Finamatik n8n workflows

Seven n8n workflows for finance and operations teams, built and tested on sample data by [Finamatik Business Solutions](https://finamatik.com/work) in Sharjah, UAE. Each one imports into n8n 1.100 or later (Import from file) and opens with a "Read me first" note that explains who it is for, what it does and how to set it up.

No credentials and no local addresses are included. Every external system is an HTTP Request against a `base` URL held in the Config node, so a workflow imports and runs against any REST backend and any node can be swapped for the native n8n node for your CRM, ERP or accounting system.

| Workflow | Canvas, execution screens and test results |
|---|---|
| [Qualify WhatsApp leads with an AI agent on the Meta Cloud API with handoff and follow-ups](whatsapp-lead-agent.json) | [finamatik.com/work/whatsapp-lead-agent](https://finamatik.com/work/whatsapp-lead-agent) |
| [Process store orders from webhook to supplier, shipping, CRM and ERP with stock checks](order-to-fulfilment.json) | [finamatik.com/work/order-to-fulfilment](https://finamatik.com/work/order-to-fulfilment) |
| [Score inbound leads with AI, reply by SMS or WhatsApp, book calendar slots and alert sales](ai-lead-response-engine.json) | [finamatik.com/work/ai-lead-response-engine](https://finamatik.com/work/ai-lead-response-engine) |
| [Extract, validate and post supplier invoices with AI and route exceptions for review](invoice-intake.json) | [finamatik.com/work/invoice-intake](https://finamatik.com/work/invoice-intake) |
| [Run month end close checks and send a management pack with AI commentary](month-end-close-pack.json) | [finamatik.com/work/month-end-close-pack](https://finamatik.com/work/month-end-close-pack) |
| [Route spend requests to approvers by threshold with deputies, reminders and escalation](approval-workflow.json) | [finamatik.com/work/approval-workflow](https://finamatik.com/work/approval-workflow) |
| [Generate content with AI agents through a QA gate and human approval before publishing](content-pipeline-qa-gate.json) | [finamatik.com/work/content-pipeline-qa-gate](https://finamatik.com/work/content-pipeline-qa-gate) |

## How the AI steps work

The AI steps call `base`/llm/complete over HTTP so the workflow has no model credential to configure. Point that step at your model endpoint, or replace it with the OpenAI or Anthropic node.

## Tests

Each workflow was run through scripted scenarios on sample data before publication (for example: a forged WhatsApp request gets a 401, a duplicate delivery is answered once, a 30 hour old conversation gets a template instead of free text, a complaint never gets an AI reply). The scenario lists and results are on the work pages linked above.

## Licence

MIT licence, copyright Finamatik Business Solutions FZE LLC. Questions and production use: info@finamatik.com.
