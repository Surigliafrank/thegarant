# Decisioni Chiave

## 2026-03-12 - Architettura iniziale
- Scelto N8N Cloud come piattaforma di automazione
- Claude Sonnet 4.5 come modello principale per GARA
- 6 agenti specializzati per viaggi (voli, hotel, ristoranti, esperienze, assicurazioni, info luogo)
- Tool gestione N8N e gestione sito per amministrazione remota

## 2026-03-12 - Code node vs Function node
- **Problema**: N8N Code node v2 NON supporta fetch() nel sandbox
- **Decisione**: Convertito tutti i tool da Code node a Function node
- **Motivo**: Function node ha this.helpers.httpRequest() per chiamate HTTP
- **Impatto**: Tutti i tool (Gestione N8N, Gestione Sito) ora usano Function node

## 2026-03-12 - CEREBRO e FRENKY
- **CEREBRO**: Memoria persistente su GitHub per non perdere contesto tra sessioni
- **FRENKY**: Comunicazione asincrona/real-time tra Telegram e Claude Code
- **Storage**: Entrambi usano il repo GitHub esistente (Surigliafrank/thegarant)
