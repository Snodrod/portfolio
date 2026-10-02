# AI Support Agent

**Focus:** agentic AI, tool interfaces and observable execution.

[Source](https://github.com/Snodrod/ai-support-agent) · [Recorded demo](https://github.com/Snodrod/ai-support-agent/blob/main/docs/demo.mp4)

A support agent for a fictional outdoor store. It handles order lookup, shipment tracking, stock, policy search, returns and callbacks using seven schema-defined tools.

The backend validates tool arguments, limits the agent loop and retries transient failures with timeouts and backoff. Returns remain pending until the customer approves them. A Server-Sent Events interface exposes tool inputs, outputs, latency, retries and model usage.

**Stack:** TypeScript, Express, zod, Anthropic SDK, vanilla JavaScript UI. An Anthropic-compatible endpoint allows alternate providers; the repository describes a demo using DeepSeek through a gateway.

**Evidence:** public source, screenshots, recorded demo and a documented suite of 13 tests using a fake model. Tests were not rerun for this portfolio.

**Boundary:** demonstration with mock store data. Real CRM/carrier integrations, authentication, rate limiting and durable sessions require production work.
