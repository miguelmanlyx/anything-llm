# AI Badgr (OpenAI-compatible)

AI Badgr is an OpenAI-compatible LLM provider that offers tier-based model access with budget-friendly pricing.

## Configuration

Set the following environment variables in your `.env` file:

```bash
LLM_PROVIDER='aibadgr'
AIBADGR_API_KEY='your-api-key'
AIBADGR_BASE_URL='https://aibadgr.com/api/v1'
AIBADGR_MODEL_PREF='premium'
AIBADGR_MODEL_TOKEN_LIMIT=4096
```

## Base URL

```
https://aibadgr.com/api/v1
```

## Authentication

Uses standard OpenAI-compatible API key authentication:

```
Authorization: Bearer <API_KEY>
```

## Model Naming (Tier-First)

AI Badgr supports two model naming conventions:

1. **Tier names** (recommended):
   - `basic` - Budget-tier models
   - `normal` - Standard-tier models  
   - `premium` - Premium-tier models (default)

2. **OpenAI model names**: AI Badgr accepts standard OpenAI model names (e.g., `gpt-4`, `gpt-3.5-turbo`) and maps them automatically to appropriate tiers.

## Example Usage

The AI Badgr provider works exactly like OpenAI's API - it's fully compatible with the OpenAI SDK and follows the same request/response format.

## Notes

- Default model is `premium` if not specified
- Supports streaming responses
- Token limits are configurable via `AIBADGR_MODEL_TOKEN_LIMIT`
- Base URL is configurable but defaults to `https://aibadgr.com/api/v1`
