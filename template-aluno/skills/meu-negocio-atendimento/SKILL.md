---
name: meu-negocio-atendimento
description: Skill de atendimento e fluxo híbrido — WhatsApp + agenda + CRM
---

# Atendimento e Fluxo Híbrido

> Skill para configurar seu COO Digital para atender leads, agendar serviços e fazer follow-up automático via WhatsApp.

## Canais de Entrada

| Canal | Como configurar |
|-------|----------------|
| **WhatsApp** | Conectar via Uazapi ou Evolution API |
| **Telegram** | Criar bot no @BotFather, conectar no OpenClaw |
| **Site/Formulário** | Webhook do formulário → OpenClaw |

## Agenda

| Sistema | Como conectar |
|---------|--------------|
| Google Calendar | API Google Calendar + service account |
| AVEC | API REST (JSON-RPC) |
| Manual | Planilha compartilhada + script |

## Funil de Atendimento

```
1. Lead entra (WhatsApp / formulário / indicação)
       ↓
2. COO classifica: calor → oferta / frio → nutrição
       ↓
3. COO oferece agendamento
       ↓
4. Cliente confirma → COO registra na agenda
       ↓
5. Lembrete automático 24h antes
       ↓
6. Pós-visita: COO pergunta satisfação (48h depois)
       ↓
7. Reativação: COO dispara oferta após 30 dias sem contato
```

## O que o COO pode fazer SOZINHO

- ✅ Responder perguntas frequentes (horário, preço, localização)
- ✅ Oferecer agendamento
- ✅ Confirmar horário
- ✅ Enviar lembrete
- ✅ Perguntar satisfação pós-serviço
- ✅ Classificar lead por perfil/interesse
- ✅ Atualizar funil no banco de dados

## O que precisa de APROVAÇÃO HUMANA

- ❌ Pagamentos e reembolsos
- ❌ Alteração de preços
- ❌ Respostas para reclamações graves
- ❌ Contratação de serviços externos

## Exemplo de Prompt para o COO

```
Você é o assistente de atendimento de [NOME DO NEGÓCIO].

REGRAS:
- Responda sempre em português, tom profissional e acolhedor
- Ofereça agendamento quando o cliente demonstrar interesse
- Consulte o histórico do cliente antes de responder
- Se o cliente tiver uma reclamação grave, alerte o humano
- Nunca informe preços sem antes confirmar o serviço desejado

FLUXO:
1. Cliente envia mensagem → identifique a intenção
2. Se for dúvida → responda com info do negócio
3. Se for interesse → ofereça agendamento
4. Se for reclamação → acalme + alerte humano
5. Atualize o status no banco de dados
```

## Integrações Típicas

- **WhatsApp:** Uazapi (webhook → OpenClaw → resposta)
- **Agenda:** API do sistema de agendamento
- **CRM:** Supabase / PostgreSQL com tabelas de clientes e agendamentos
- **Funil:** ReativaZap ou similar para follow-up automático

## Checklist de Implantação

- [ ] Canal de entrada configurado (WhatsApp/Telegram)
- [ ] COO consegue consultar agenda
- [ ] COO consegue criar agendamento
- [ ] COO tem acesso ao histórico do cliente
- [ ] Follow-up automático funcionando
- [ ] Lembrete 24h antes configurado
- [ ] Pós-visita programada
- [ ] Humano recebe alerta em caso de exceção

---

*Skill baseada no case real do Kihon Hair Studio · Adapte para seu negócio*
