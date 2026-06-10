# n8n-portfolio

Collection of n8n automation workflows built for portfolio purposes.

## Workflows

### 1. Monitor USD/JPY
Monitors the USD/JPY forex pair every 30 minutes using a free exchange rate API. Sends Discord alerts when the price is above or below a defined threshold.

**Nodes:** Schedule Trigger → HTTP Request → If → Discord (webhook)
**API:** open.er-api.com (free, no API key required)

### 2. AI Act News Digest
Fetches the latest AI Act and compliance news every morning via RSS feed. Uses Groq LLM to summarise each article and sends a formatted digest to Discord.

**Nodes:** RSS Feed Trigger → Code (JS) → HTTP Request (Groq API) → Discord
**API:** Groq (free tier)

### Error Trigger (shared)
Monitors all workflows above. Sends a Discord alert with the workflow name and error message if any execution fails.
