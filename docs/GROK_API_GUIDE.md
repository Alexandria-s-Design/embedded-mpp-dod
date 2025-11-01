# Grok 4 API Integration Guide

## Overview

**Status**: ✅ Configured and Ready
**Helper**: `scripts/api-helpers/grok_helper.py`
**API Key**: Stored in `.env` as `GROK_API_KEY`
**Model**: Grok 4 (released July 2025)

Grok 4 is xAI's latest advanced language model with massive context windows, recent information access (Nov 2024 knowledge cutoff), vision capabilities, native tool use, and strong reasoning abilities.

## Available Models

1. **grok-4** - Main Grok 4 model (recommended, 256K context)
2. **grok-4-0709** - Specific version (July 2025 release)
3. **grok-vision-beta** - Vision-enabled model for image analysis
4. **grok-4-fast-reasoning** - Fast model with reasoning (2M context window!)
5. **grok-4-fast-non-reasoning** - Fast model without reasoning (2M context window)

## Capabilities

- ✅ Advanced reasoning and problem-solving
- ✅ Recent information access (knowledge through November 2024)
- ✅ Massive context windows (256K standard, 2M for fast models)
- ✅ Vision analysis (image understanding, OCR, screenshot analysis)
- ✅ Native tool use integration
- ✅ Code generation and debugging
- ✅ Streaming responses for real-time output

## When to Use Grok 4

**Use Grok 4 for:**
- Recent information (knowledge through November 2024)
- Processing very long documents (256K-2M token context)
- Complex reasoning tasks
- Image analysis and vision tasks
- Code review and debugging
- Long-form content generation
- Technical documentation analysis
- Native tool/function calling

**Compared to other APIs:**
- **vs OpenAI GPT-4o**: Grok 4 has 2x context (256K vs 128K), more recent knowledge, 2M option
- **vs Claude**: Grok 4 has Nov 2024 knowledge (more recent), massive 2M context option
- **vs OpenRouter free models**: Significantly higher quality, more capable, costs money but worth it

## Setup

### 1. Get API Key

Visit: https://console.x.ai/
- Sign in with X/Twitter account
- Navigate to API Keys section
- Create new API key

### 2. Add to Environment

Already configured in `.env`:
```bash
GROK_API_KEY=xai-K1xq1fOvoO4nOFPEbCK3yNEILrzh1ortXqFK6kw689EwTQUOucQgfUfWaD0q3dvNegcKb6l2icnOwbIm
```

### 3. Install Dependencies

```bash
pip install openai python-dotenv
```

## Usage Examples

### Basic Chat Completion

```python
from scripts.api_helpers.grok_helper import GrokHelper

helper = GrokHelper()

# Simple one-shot question
response = helper.simple_chat("What are the latest developments in AI?")
print(response)
```

### Advanced Chat with Full Control

```python
# Multi-turn conversation
messages = [
    {"role": "system", "content": "You are a helpful coding assistant."},
    {"role": "user", "content": "Explain async/await in Python"}
]

response = helper.chat(
    messages=messages,
    model="grok-4",
    temperature=0.7,
    max_tokens=1000
)

print(response["content"])
print(f"Tokens used: {response['usage']['total_tokens']}")
```

### Vision Analysis

```python
# Analyze an image
analysis = helper.analyze_image(
    image_url="https://example.com/screenshot.png",
    prompt="What errors do you see in this code screenshot?",
    model="grok-vision-beta"
)

print(analysis)
```

### Streaming Responses

```python
# Stream responses in real-time
messages = [
    {"role": "user", "content": "Write a Python function to sort a list"}
]

print("Grok is responding: ", end="")
for chunk in helper.chat_stream(messages):
    print(chunk, end="", flush=True)
print()
```

## Claude Code Integration

When Claude Code suggests using Grok, you'll see:

```
Claude: "Would you like me to use Grok for [task]?
         This will use your GROK_API_KEY for real-time information access.
         Estimated cost: ~$0.02-0.05 per query"

User: "Yes"

Claude: [Uses grok_helper.py with Grok 4 to complete task]
```

## Cost Optimization

**Pricing** (Grok 4, as of 2025):
- Input: $3 per 1M tokens
- Output: $15 per 1M tokens
- Cached tokens: $0.75 per 1M tokens
- Typical query: $0.02-0.05

**Tips to save money:**
- Use `grok-4` (standard) for most tasks (256K context)
- Use `grok-4-fast-reasoning` for very long documents (2M context)
- Use `grok-vision-beta` only when analyzing images
- Set reasonable `max_tokens` limits
- Use for tasks that benefit from Nov 2024 knowledge
- Consider OpenRouter free models for general/older knowledge tasks

## Common Use Cases

### 1. Real-Time Research

```python
helper = GrokHelper()
result = helper.simple_chat(
    "What are the latest grant opportunities from the Department of Education (Jan 2025)?"
)
```

### 2. Code Review

```python
code = """
def calculate_total(items):
    total = 0
    for item in items:
        total += item.price
    return total
"""

review = helper.simple_chat(f"Review this code and suggest improvements:\n\n{code}")
```

### 3. Image Analysis

```python
# Analyze a screenshot
analysis = helper.analyze_image(
    image_url="file:///C:/Users/MarieLexisDad/Pictures/Screenshots/error.png",
    prompt="What error message is shown and how can I fix it?"
)
```

### 4. Complex Reasoning

```python
problem = """
I need to design a database schema for a school management system
that handles students, courses, enrollments, grades, and teachers.
What's the best approach?
"""

solution = helper.simple_chat(problem)
```

## Testing

```bash
# Run full test suite
python scripts/api-helpers/test_grok.py

# Quick connection test
python scripts/api-helpers/grok_helper.py
```

## Troubleshooting

### API Key Issues

```python
# Check if key is loaded
import os
from dotenv import load_dotenv

load_dotenv()
print(os.getenv("GROK_API_KEY"))  # Should show your key
```

### Connection Issues

```python
helper = GrokHelper()
if helper.test_connection():
    print("Connected!")
else:
    print("Check API key and internet connection")
```

### Model Availability

```python
# List available models
helper = GrokHelper()
print(helper.list_models())
```

## API Reference

### GrokHelper Class

**Methods:**

- `chat(messages, model, temperature, max_tokens, stream)` - Full chat completion
- `simple_chat(user_message, model)` - Quick single message
- `analyze_image(image_url, prompt, model)` - Vision analysis
- `chat_stream(messages, model, temperature)` - Streaming responses
- `list_models()` - Available model list
- `get_model_info()` - Capabilities and info
- `test_connection()` - Verify API access

## Best Practices

1. **Choose the right model:**
   - Use `grok-4` for standard tasks (256K context)
   - Use `grok-4-fast-reasoning` for huge documents (2M context)
   - Use `grok-vision-beta` only when analyzing images

2. **Optimize costs:**
   - Set appropriate `max_tokens`
   - Cache results when possible
   - Use for tasks requiring real-time data

3. **Handle errors gracefully:**
   ```python
   try:
       response = helper.simple_chat("Your question")
   except Exception as e:
       print(f"Grok API error: {e}")
   ```

4. **Leverage real-time capabilities:**
   - Current events and news
   - Recent product launches
   - Latest research and publications
   - Up-to-date documentation

## Integration with Alexandria's Design Workflow

**Revenue Applications:**

1. **Client Research** - Real-time grant opportunities, latest education trends
2. **Content Creation** - Up-to-date blog posts, current best practices
3. **Technical Support** - Debug client issues with vision analysis
4. **Course Development** - Latest industry developments, current standards
5. **Competitive Analysis** - Recent competitor launches, market changes

**Automation Ideas:**

- Use with n8n to auto-research grant opportunities weekly
- Integrate with Monday.com for task generation from latest trends
- Combine with Google Workspace to analyze client screenshots
- Stream responses for live educational webinars

## Resources

- **API Documentation**: https://docs.x.ai/api
- **Console**: https://console.x.ai/
- **Pricing**: https://x.ai/pricing
- **Status**: https://status.x.ai/

## Support

For issues with Grok API:
1. Check API key in `.env`
2. Run `python scripts/api-helpers/test_grok.py`
3. Verify internet connection
4. Check https://status.x.ai/ for outages
5. Review API docs at https://docs.x.ai/api
