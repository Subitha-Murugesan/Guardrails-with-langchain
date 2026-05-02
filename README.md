# Guardrails-with-langchain
Building safe AI agents with LangChain through layered guardrails for input filtering, PII protection, human-in-the-loop approvals, output validation, and domain-specific safety controls.


This README is for `Guardrails.ipynb`, a hands-on notebook that demonstrates common guardrail patterns for LLM applications using LangChain.

## What It Covers

- Deterministic guardrails using keyword and rule-based checks
- Model-based guardrails using an LLM safety classifier
- Built-in PII detection middleware
- Human-in-the-loop middleware for sensitive actions
- Custom before-agent input filters
- Custom after-agent output safety checks
- Layered guardrails that combine multiple protections

## Setup

Create a `.env` file in this directory with the API key for your configured provider:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
```

If you use OpenAI directly instead of OpenRouter, use:

```env
OPENAI_API_KEY=your_openai_api_key
```

## Install Dependencies

Install the core packages used by the notebook:

```bash
pip install langchain langchain-openai langchain-openrouter langgraph python-dotenv
```

## Run

Start Jupyter:

```bash
jupyter notebook Guardrails.ipynb
```

Then run the cells from top to bottom.

## Notes

The deterministic examples run locally and do not need an API key. The model-based and agent middleware examples call an LLM provider, so they require a valid API key with available credits.

