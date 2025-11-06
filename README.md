# SentialFlow
SentinelFlow quietly reduces alert noise by turning raw signals into instant priority decisions — so humans spend focus only where impact truly matters.

SentinelFlow is an autonomous SOC alert triage layer designed to reduce analyst overload and wasted time on low-value notifications. Today, SIEMs generate thousands of alerts, but 70–80% are noise or non-actionable. Analysts still have to open each alert, enrich it, check context, and manually decide if it matters. That is the bottleneck — not detection.

SentinelFlow solves this by performing machine-fast triage after detection. When an alert arrives, SentinelFlow enriches it automatically using OSINT (VirusTotal) and applies a local lightweight LLM (Mistral via Ollama) to decide severity, using structured prompt constraints. No cloud inference, no token costs, no data privacy risk. The entire decision pipeline is built with n8n to ensure simplicity, repeatability, and transparency.

The output is a clean, human-readable severity verdict delivered to a communication channel (Discord) within seconds. Analysts only see alerts that actually require attention — instead of clicking through noise. This PoC deliberately targets one alert type (domain-based events) to maintain focus and feasibility, but the architecture generalizes to IP, URL, file hash, and log sources.
