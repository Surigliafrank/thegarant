# Problemi e Soluzioni

## executeWorkflowTrigger - "workflow has issues"
- **Problema**: Sub-workflow chiamati da toolWorkflow fallivano con "The workflow has issues"
- **Causa**: Il nodo executeWorkflowTrigger aveva parameters: {} vuoto
- **Soluzione**: Aggiungere parameters: { inputSource: 'passthrough' } a TUTTI i trigger
- **Data**: 2026-03-12

## fetch is not defined
- **Problema**: Code node v2 non ha fetch() nel sandbox
- **Causa**: Il sandbox del Code node non include fetch, require, o altri globali Node.js
- **Soluzione**: Convertire da Code node (v2) a Function node (v1) che ha this.helpers.httpRequest()
- **Data**: 2026-03-12

## Telegram parse entities error
- **Problema**: "Can't find end of the entity starting at byte offset X"
- **Causa**: GARA generava markdown con tag non chiusi (* o ` senza chiusura)
- **Soluzione**: Rimosso parse_mode dal nodo Telegram - Invia Risposta (ora plain text)
- **Data**: 2026-03-12

## Tool name invalid characters
- **Problema**: "Value is not a valid alphanumeric string, only letters, numbers and underscore allowed"
- **Causa**: Il codice collega_agente generava nomi con trattini (marketing_-_copywriter)
- **Soluzione**: Sanitizzare nomi con .replace(/[^a-z0-9]/g, '_')
- **Data**: 2026-03-12

## N8N API settings error
- **Problema**: "settings must NOT have additional properties"
- **Causa**: Inviare settings con proprietà extra (executionTimeout, etc.)
- **Soluzione**: Usare SOLO settings: { executionOrder: 'v1' }
- **Data**: 2026-03-12

## Telegram webhook 404
- **Problema**: Dopo attivazione via API, webhook Telegram ritorna 404
- **Causa**: Attivazione via API non registra webhook su N8N Cloud
- **Soluzione**: Disattivare e riattivare manualmente dall'UI di N8N
- **Data**: 2026-03-12
