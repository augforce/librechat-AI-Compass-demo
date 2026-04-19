# LibreChat Smart Model Guidance System -  AI Compass
A user-friendly AI model selection system for LibreChat that helps staff choose the most appropriate AI model for their specific task, improving both output quality and cost efficiency.

<img width="1717" height="1034" alt="Screenshot 2026-04-19 at 10 22 47 AM" src="https://github.com/user-attachments/assets/b7e824d4-097a-41d7-90dc-9c4c4f36c5ef" />

## The Problem
Staff members often struggle to choose between multiple AI models:
- Unclear which model is best for their specific use case
- Tendency to either always use the most expensive model (wasteful) or cheapest model (poor results)
- No guidance on model capabilities and strengths
- Confusion about technical model names (gpt-4o vs claude-3.5-sonnet vs gemini-pro)

## The Solution
**Task-Based Model Recommendations** displayed at the top of the model selector:

<img width="332" height="542" alt="Screenshot 2026-04-19 at 10 04 55 AM" src="https://github.com/user-attachments/assets/d49042df-019a-4a41-8b55-66d7ec77fd75" />

### Guided Assistant Options

| Assistant | Model | Optimized For |
|-----------|-------|---------------|
| ❓ **General Use** | GPT-5.4 | Quick questions, simple tasks, general chat |
| 🎧 **Support Assistant** | GPT-5.4-mini | Tech Support, FAQ answers |
| ✨ **Creative Pro** | Claude Sonnet 4.6 | Marketing copy, creative writing, brainstorming |
| 💻 **Code Expert** | Claude Opus 4.7 | Programming, debugging, technical documentation |
| 📊 **Document Analyzer** | GPT-5.4 | PDF analysis, research, long document review |

**Plus:** All original models remain accessible for power users who know exactly what they need. Speech-to-test, based on OpenAI's Whisper, included in prompt window.

## Benefits

### For End Users
- ✅ **Clear guidance** on which assistant to use
- ✅ **Faster decisions** - no need to research model capabilities
- ✅ **Better results** - right tool for the right job
- ✅ **Reduced cognitive load** - simple, task-based choices

### For the Organization
- 💰 **Cost optimization** (60-80% reduction) as a side benefit
- 📊 **Better output quality** from appropriate model selection
- 🎯 **Reduced trial-and-error** and wasted queries
- 📈 **Increased AI adoption** through improved user experience

### For IT/Admin
- 🛠️ **Easy to maintain** - single YAML configuration
- 📝 **Customizable** - adjust assistants based on usage patterns
- 🔍 **Transparent** - users still have access to all models
- 🔄 **Flexible** - can add/remove/modify assistants anytime

## Setup

### Prerequisites
- Docker Desktop installed
- LibreChat instance running
- API keys for desired providers:
  - OpenAI (required)
  - Anthropic (optional, for Claude models)
  - Google (optional, for Gemini models)

### Configuration Files

- `librechat yaml` - Main configuration with model specs
- `edited .env` - Template for environment variables; API Keys removed

### Model Selection Analysis
❓ **General Use** | GPT-5.4 |
Recently released, the standard GPT-5.4 is widely considered the cleanest default for broad, general-purpose work. If staff need quick, reliable answers for everyday tasks, this is a fantastic go-to. (If you want an even cheaper, faster option for very simple questions, GPT-5.4 mini is their newest lightweight model).

🎧 **Support Assistant** | GPT-5.4-mini |
For tech/internal policy support, you will likely be loading a massive PDF of company policies, troubleshooting steps, and IT protocols into the system prompt. Since every user asks questions against that same document, caching is your best friend. Lightning-fast, accurate answers to standard IT questions at a fraction of the cost of the main models.

✨ **Creative Pro** | Claude Sonnet 4.6 |
Claude 4.6 Sonnet has a much higher "EQ" (emotional intelligence). It excels at mimicking human nuance, varying sentence structure, and following specific brand voice instructions without sounding robotic. This saves your staff massive amounts of editing time, making it highly efficient. This will ensure your staff has the best tool for drafting compelling, human-sounding copy.

💻 **Code Expert** | Claude Opus 4.7 |
Anthropic released Claude Opus 4.7 a few days ago on April 16, 2026, and it is currently the undisputed heavyweight champion for software engineering. If your staff is generating code, debugging, or building software architectures, Opus 4.7 completely outclasses the competition (including GPT-5.4). 

📊 **Document Analyzer** | GPT-5.4 |
When analyzing modern documents, your staff isn't just parsing plain text—they need to extract insights from embedded charts, graphs, and complex data tables. OpenAI's native vision architecture in GPT-5.4 is currently unparalleled at accurately "seeing" and interpreting visual data from PDFs. While Claude models are brilliant at text reasoning, GPT-5.4 is far less likely to hallucinate the numbers inside a complex bar chart.
