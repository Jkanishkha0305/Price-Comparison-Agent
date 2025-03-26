# Architecture — Price-Comparison-Agent

> 🏆 CerebrasxCrew AI Hackathon Winner

## Agent Pipeline

```
  User Query: "Find me the cheapest iPhone 15 Pro across major retailers"
       │
       ▼
  ┌────────────────────────────────────────────────┐
  │           CrewAI Multi-Agent System            │
  │                                                │
  │  Agent 1: Search Agent                        │
  │  └─ Cerebras LLM (ultra-fast inference)       │
  │     Searches Amazon, BestBuy, Walmart, etc.   │
  │                                                │
  │  Agent 2: Price Extractor                     │
  │  └─ Parses product pages, extracts prices     │
  │     Handles different page structures         │
  │                                                │
  │  Agent 3: Comparison Analyst                  │
  │  └─ Cerebras: builds comparison table         │
  │     Accounts for shipping, taxes, promotions  │
  │                                                │
  │  Agent 4: Recommendation Agent               │
  │  └─ Final verdict with reasoning              │
  └────────────────────────────────────────────────┘
       │
       ▼
  Structured output: price table + best deal recommendation
```

## Why Cerebras?

Cerebras provides ultra-low latency LLM inference (sub-100ms) — critical for a price comparison agent that needs to make many rapid sequential decisions across multiple retailers.
