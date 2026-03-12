# Sistema GARA - Configurazione

## Architettura
- **GARA**: Assistente privato Telegram per Francesco (ID: SrZJYCPSYOUSRdmh)
- **N8N Cloud**: https://thegarant.app.n8n.cloud
- **Sito**: thegarant.com - statico HTML/CSS, deploy da GitHub
- **AI**: Claude Sonnet 4.5 (GARA), Claude Haiku 4.5 (agenti leggeri)

## Workflow IDs
| Workflow | ID | Stato |
|----------|-----|-------|
| GARA Telegram | SrZJYCPSYOUSRdmh | Attivo |
| Website Chat | kapzcdq1w2ot5tMD | - |
| Agent Voli | qUSdLVeVNwdnMIXE | - |
| Agent Hotel | g4CLmhEHvQtiXy6z | - |
| Agent Ristoranti | 1dZ1VeGZDQwTXnFa | - |
| Agent Esperienze | g36iB9HH09VWNlhE | - |
| Agent Assicurazioni | aaziC8q8xdbKhif8 | - |
| Agent Info Luogo | D9kx5HpIpaudCIBB | - |
| Tool Gestione N8N | yrwtDMHZbMyqorVi | - |
| Tool Gestione Sito | cmcdkdMPoiugZMtU | - |
| Tool CEREBRO | (da creare) | - |
| Tool FRENKY | (da creare) | - |

## Credenziali N8N
| Tipo | ID |
|------|-----|
| Telegram Bot | 3DQ6ODGn1jHuhsBX |
| Anthropic API | 18dFk87aqQnRQ4ub |

## Sicurezza
- Telegram ID Francesco: 1077537366
- PIN azioni distruttive: configurato (non salvato qui per sicurezza)
- 6 livelli: Telegram ID, PIN, HTML sanitization, whitelist, git versioning, rate limit

## GitHub
- Repo: Surigliafrank/thegarant
- Deploy automatico su ogni push
