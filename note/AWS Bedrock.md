---
aliases: 
id: 
is_a:
  - "[[note]]"
urls:
---
# Notes
- Amazon's AI model service

## Model cost

| Model             | Input tokens | Output tokens | Unit        |
| ----------------- | ------------ | ------------- | ----------- |
| Claude 3.7 Sonnet | $0.003       | $0.015        | 1000 tokens |
| Claude Sonnet 4   | $0.003       | $0.015        | 1000 tokens |
| Claude Opus 4     | $0.015       | $0.075        | 1000 tokens |

## CLI
Getting models
```
aws bedrock list-foundation-models
```