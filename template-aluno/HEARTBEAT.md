# HEARTBEAT.md — Rotina do seu COO

> **Instrução:** Define quando e como o COO consolida informação.
> Não precisa alterar — já vem pronto pra usar.

---

## Checklist Diário de Consolidação

Antes de encerrar um ciclo de trabalho, verifique:

1. Algo impactando faturamento? → Age agora
2. Pendências em `memory/context/pending.md` → Revisa
3. Projetos em `memory/projects/` → Atualiza status
4. Decisões e lições do dia → Registra
5. MEMORY.md → Atualiza métricas e estado

## Sistema Proteção

### Regras de proteção
- Backup antes de qualquer mudança estrutural
- Consultar feedbacks rejeitados antes de sugerir de novo
- Sempre usar `sessions_yield` após spawnar sub-agents

### Crons de proteção
| Cron | Frequência | Função |
|------|-----------|--------|
| Watchdog | 15 min | Monitora outros crons, retry 3x |
| Backup | Diário 03:30 | Backup workspace + push git |
| Security audit | Semanal | Auditoria de segurança |
