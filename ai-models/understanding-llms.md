# Understanding Large Language Models (LLMs)

[← Back to Main Documentation](../README.md)

This guide explains the fundamentals of AI language models, helping you choose the right model and use it effectively.

---

## What is an LLM?

A **Large Language Model (LLM)** is an artificial intelligence system trained on vast amounts of text data. LLMs can:
- Understand and generate human-like text
- Answer questions based on their training
- Write, edit, and summarize content
- Translate languages
- Assist with coding and technical tasks
- Analyze and reason about information

LLMs power conversational AI, content generation, and knowledge retrieval across industries.

---

## Key Concepts

### Tokens

**What is a token?**
A token is a piece of text the AI processes. Tokens are roughly equivalent to:
- **1 token = ~0.75 words** (in English)
- **1 word = ~1.3 tokens** (average)

**Examples**:
- "Hello world" = 2 tokens
- "Artificial intelligence" = 2 tokens
- "KeystoneAgentic is amazing" = 4 tokens

**Why tokens matter**:
- Pricing is based on tokens (input + output)
- Context windows are measured in tokens
- Quota limits are tracked in tokens

**Types of tokens**:
- **Input Tokens**: What you send to the AI (your prompts and conversation history)
- **Output Tokens**: What the AI generates in response
- **Total Tokens**: Input + Output (used for billing)

---

### Context Window

**What is a context window?**
The maximum amount of text (in tokens) an AI model can process in a single request.

**Example**:
- **Model with 8K context window**: Can process ~6,000 words total (input + output)
- **Model with 128K context window**: Can process ~96,000 words total

**What fits in the context window**:
- Your current prompt
- Previous messages in the conversation
- System instructions
- Retrieved documents (for RAG)
- The AI's response

**Why it matters**:
- Larger context windows allow longer conversations without losing history
- You can include more documents in RAG queries
- Complex tasks requiring lots of context need larger windows

**Common context window sizes**:
- **4K - 8K tokens**: Short conversations, simple tasks
- **16K - 32K tokens**: Medium conversations, multi-turn dialogue
- **128K - 200K tokens**: Long conversations, entire documents, extensive RAG
- **1M+ tokens**: Experimental models, massive document analysis

**What happens when you exceed the context window?**
- Older messages are dropped from the conversation
- The AI "forgets" earlier parts of the discussion
- You may need to start a new conversation or summarize prior context

---

### Parameters and Model Size

**What are parameters?**
Parameters are the internal settings the AI learned during training. More parameters generally mean:
- Better understanding of complex topics
- More nuanced responses
- Higher computational cost
- Slower response times

**Common parameter counts**:
- **7B - 13B parameters**: Fast, efficient, good for simple tasks
- **70B - 180B parameters**: Balanced performance and speed
- **300B+ parameters**: Highest quality, slower, more expensive

**Bigger isn't always better**:
- Small models are faster and cheaper
- Large models handle complex reasoning better
- Choose based on your task complexity, not just size

---

### Model Capabilities

Different models have different features:

**Streaming**
- AI sends responses word-by-word as they're generated
- You see the response in real-time
- Better user experience for long responses

**Function Calling**
- AI can call external tools and APIs
- Useful for integrations (search engines, databases, calculators)
- Structured output for automated workflows

**Vision**
- AI can analyze images
- Describe photos, extract text from images, answer questions about visuals
- Not all models support vision

**Reasoning / Chain-of-Thought**
- AI shows its "thinking" process before answering
- Better for complex logic, math, and problem-solving
- Usually slower and more expensive

---

## Model Types

### Standard Models (Fast Models)

**Characteristics**:
- Generate responses immediately
- No visible "thinking" process
- Fast and cost-effective
- Best for most tasks

**Use cases**:
- General conversation
- Content writing
- Summarization
- Translation
- Coding assistance (straightforward problems)
- Customer support

---

### Reasoning Models (Thinking Models)

**Characteristics**:
- Spend time "thinking" before responding
- Show chain-of-thought reasoning
- Better at complex logic and problem-solving
- Slower and more expensive

**Use cases**:
- Complex math and logic problems
- Multi-step reasoning tasks
- Scientific analysis
- Advanced coding (debugging complex systems)
- Strategic planning
- Research and analysis

**Cost-benefit trade-off**:
- Reasoning models cost **2-5x more** than standard models
- They take **longer to respond** (sometimes 10-30 seconds)
- Use them only when complexity justifies the cost

---

### Specialized Models

**Code-Specialized Models**:
- Optimized for programming tasks
- Better at understanding code syntax and patterns
- Often trained on large code repositories

**Embedding Models**:
- Convert text into numerical vectors
- Used for semantic search and RAG
- Power document retrieval systems

**Multimodal Models**:
- Handle text + images (and sometimes audio/video)
- Can analyze visual content and respond in text
- Useful for OCR, image description, visual Q&A

**Multilingual Models**:
- Better at non-English languages
- Handle translation and cross-lingual tasks
- Trained on diverse language datasets

---

## Choosing the Right Model

### Finding the Best Models

**AI progress is exponential.** Model rankings change constantly as new models are released and improved. What's considered "best" today may be outperformed next month.

**Use these leaderboards to find current top performers**:

**General Performance Rankings**:
- **LM Arena Leaderboard**: [https://lmarena.ai/leaderboard/](https://lmarena.ai/leaderboard/)
  - Community-driven model rankings based on blind comparisons
  - Updated frequently with new models
  - Shows which models users prefer in real conversations

- **OpenRouter Rankings**: [https://openrouter.ai/rankings](https://openrouter.ai/rankings)
  - Performance metrics across all available models
  - Cost, speed, and quality comparisons
  - Real-time availability and uptime data

**Specialized Leaderboards**:
- **Vellum LLM Leaderboard**: [https://www.vellum.ai/llm-leaderboard](https://www.vellum.ai/llm-leaderboard)
  - Task-specific benchmarks
  - Helps identify models best suited for different use cases

- **Artificial Analysis**: [https://artificialanalysis.ai/leaderboards/models](https://artificialanalysis.ai/leaderboards/models)
  - Performance vs. cost analysis
  - Latency and throughput comparisons
  - Quality benchmarks across dimensions

- **Scale AI Leaderboard**: [https://scale.com/leaderboard](https://scale.com/leaderboard)
  - Rigorous academic benchmarks
  - Domain-specific evaluations (coding, math, reasoning)

**Why leaderboards matter**:
- Rankings change monthly (or even weekly)
- New models are constantly released
- Performance improvements are rapid and unpredictable
- What was "state-of-the-art" 3 months ago may be mid-tier today

**Pro tip**: Check leaderboards regularly and don't get attached to specific models. The AI landscape evolves quickly.

---

### Decision Framework

**For simple, high-volume tasks**:
- Choose **fast, cheap models** from the lower-cost tier
- Prioritize speed and cost-efficiency
- Check leaderboards for "best value" models
- Examples: Customer support, simple Q&A, translations

**For balanced performance**:
- Choose **mid-tier models** with good quality-to-cost ratio
- Look at the middle of leaderboards for reliable performers
- Good for most general-purpose tasks
- Examples: Content generation, coding assistance, general conversation

**For complex reasoning**:
- Choose **reasoning models** that rank high on math/logic benchmarks
- Justify higher cost with task complexity
- Check specialized benchmarks for reasoning and problem-solving
- Examples: Advanced math, strategic analysis, complex debugging

**For large documents**:
- Choose models with **large context windows** (128K+ tokens)
- Filter by context length in model discovery
- Essential for full document analysis
- Examples: Contract review, research papers, extensive RAG

**For vision tasks**:
- Choose **multimodal models** with vision capabilities
- Check vision-specific benchmarks
- Examples: Image analysis, OCR, visual Q&A

---

### Understanding Model Strengths

Different models excel at different tasks. Leaderboards help you identify:

**Coding Excellence**:
- Look for high scores on HumanEval, MBPP benchmarks
- Code-specialized models often outperform general models
- Check Stack Overflow and programming-specific evaluations

**Mathematical Reasoning**:
- GSM8K and MATH benchmarks indicate math capability
- Reasoning models typically dominate these benchmarks
- Important for quantitative analysis and problem-solving

**Instruction Following**:
- MT-Bench and AlpacaEval measure how well models follow instructions
- Critical for structured tasks and workflows
- High scores mean more reliable, predictable outputs

**Creative Writing**:
- Subjective, but LM Arena shows user preferences
- "Creative" tasks often benefit from higher temperature settings
- Larger models tend to have more nuanced language generation

**Factual Accuracy**:
- TruthfulQA benchmark measures factual correctness
- RAG can enhance accuracy regardless of base model
- Cross-reference critical facts even with top-ranked models

**Multilingual Capability**:
- Check benchmarks in your target language
- Some models specialize in specific language families
- Performance can vary dramatically across languages

---

### Cost Considerations

**Pricing varies by**:
- **Input tokens**: What you send (usually cheaper)
- **Output tokens**: What the AI generates (usually more expensive)
- **Model tier**: Reasoning models cost more than standard models
- **Model size**: Larger parameter models cost more

**Approximate pricing tiers** (per 1M tokens):
- **Budget tier**: $0.10 - $0.50 per 1M tokens
- **Standard tier**: $1 - $5 per 1M tokens
- **Premium tier**: $5 - $15 per 1M tokens
- **Reasoning tier**: $10 - $60 per 1M tokens

**Use leaderboards to optimize cost**:
- **Artificial Analysis** shows cost-per-quality metrics
- Find the cheapest model that meets your quality threshold
- Balance speed, cost, and accuracy for your use case

**Optimization tips**:
- Use cheaper models for simple tasks
- Shorten prompts when possible (fewer input tokens)
- Limit conversation history to reduce input tokens
- Cache repeated prompts (when supported)
- Use streaming to stop responses early if needed
- Test with budget models before committing to premium ones

---

## Model Performance Factors

### The Pace of AI Progress

**AI development is exponential, not linear.**

**What this means**:
- A model that's "best" today may be surpassed in weeks
- Performance improvements happen faster than in any other technology field
- Capabilities that were impossible 6 months ago are now commonplace
- Pricing often drops as newer, better models are released

**Practical implications**:
- Don't over-invest in learning one specific model
- Focus on understanding model categories and use cases
- Stay flexible—be ready to switch models as the landscape shifts
- Regularly check leaderboards (monthly at minimum)
- Experiment with new models as they're released

**Historical perspective**:
- 2022: Models struggled with basic reasoning
- 2023: Models achieved near-human performance on many benchmarks
- 2024: Reasoning models, multimodal capabilities, and 1M+ token contexts became standard
- 2025: The pace continues to accelerate

**Future-proofing your AI usage**:
- Build workflows that can swap models easily
- Use abstraction layers (like KeystoneAgentic) rather than direct API integrations
- Test new models regularly to stay current
- Monitor leaderboards and industry news

---

### Uptime and Availability

Models can experience downtime or degraded performance. KeystoneAgentic shows:
- **Uptime percentage**: Reliability in the last 30 minutes
- **Real-time status**: Whether the model is currently available

**Best practice**: Sync multiple models as backups in case your primary model is down.

---

### Latency (Response Time)

**Factors affecting speed**:
- **Model size**: Larger models are slower
- **Context length**: Longer prompts take longer to process
- **Reasoning**: Thinking models are slower than standard models
- **Provider load**: High demand can slow responses

**Typical response times**:
- **Fast models**: 1-3 seconds
- **Standard models**: 3-10 seconds
- **Reasoning models**: 10-60 seconds

**Streaming helps**: Even if total time is long, streaming shows progress immediately.

**Check latency benchmarks**:
- Artificial Analysis provides detailed latency data
- Time-to-first-token (TTFT) measures responsiveness
- Tokens-per-second (TPS) measures throughput

---

### Quality and Accuracy

**No model is perfect**:
- AI can generate incorrect information (hallucinations)
- Responses vary based on phrasing
- Quality depends on the training data

**Improving accuracy**:
- Use clear, specific prompts
- Provide examples in your prompt (few-shot learning)
- Use RAG to ground responses in your documents
- Choose high-quality models for critical tasks (check leaderboards)
- Verify factual claims independently
- Use reasoning models for complex logic

**Benchmarks for quality**:
- **MMLU** (Massive Multitask Language Understanding): General knowledge
- **TruthfulQA**: Factual accuracy
- **HumanEval**: Coding correctness
- **MT-Bench**: Instruction following and dialogue quality

---

## Advanced Concepts

### Temperature

**What it does**: Controls randomness in AI responses.
- **Low temperature (0.0 - 0.3)**: Deterministic, consistent, factual
- **Medium temperature (0.5 - 0.7)**: Balanced creativity and consistency
- **High temperature (0.8 - 1.0)**: Creative, varied, unpredictable

**Use cases**:
- **Low**: Factual Q&A, data extraction, code generation
- **Medium**: General conversation, content writing
- **High**: Creative writing, brainstorming, storytelling

---

### Top-P (Nucleus Sampling)

**What it does**: Limits token selection to the most probable options.
- **Low top-p (0.1 - 0.5)**: Focused, coherent
- **High top-p (0.9 - 1.0)**: Diverse, exploratory

**Relationship with temperature**:
- Usually, adjust **one or the other**, not both
- Top-p is often preferred over temperature for fine control

---

### Max Tokens (Output Length)

**What it does**: Limits how long the AI's response can be.
- **Short (100-500 tokens)**: Quick answers, summaries
- **Medium (500-2000 tokens)**: Detailed explanations
- **Long (2000+ tokens)**: Essays, extensive analysis

**Best practice**: Set based on expected response length to save costs and avoid overly verbose answers.

---

### Frequency and Presence Penalties

**Frequency Penalty**: Reduces repetition of words/phrases already used.
- Higher values = less repetition
- Use for creative writing to avoid redundancy

**Presence Penalty**: Encourages introducing new topics.
- Higher values = more diverse content
- Use for brainstorming and exploration

---

## Limitations of LLMs

### What LLMs Cannot Do

**Real-time information**:
- LLMs are trained on data up to a certain date (cutoff)
- They don't know current events unless you provide that context
- Use RAG or function calling to add real-time data

**Mathematical precision**:
- LLMs approximate math but can make errors
- Use calculators or code execution for precise calculations
- Reasoning models are better but not perfect

**Deterministic logic**:
- LLMs are probabilistic, not deterministic
- Same prompt can yield different responses
- Use low temperature for consistency

**Memory across sessions**:
- LLMs don't remember previous conversations unless you provide history
- Conversations in KeystoneAgentic maintain history, but switching conversations means starting fresh

---

### Common Pitfalls

**Hallucinations**:
- AI confidently states incorrect information
- **Mitigation**: Use RAG, verify facts, ask for sources, use high-ranked models on TruthfulQA

**Bias**:
- LLMs reflect biases in their training data
- **Mitigation**: Be aware, critically evaluate responses, use diverse models

**Context limits**:
- Long conversations exceed context windows
- **Mitigation**: Summarize earlier parts, start new conversations, use models with larger contexts

**Prompt sensitivity**:
- Small changes in wording can drastically change responses
- **Mitigation**: Iterate on prompts, use clear instructions, test variations

---

## Best Practices

### Writing Effective Prompts

**Be specific**:
- Vague: "Tell me about marketing"
- Specific: "List 5 digital marketing strategies for a B2B SaaS company"

**Provide context**:
- Include background information
- Specify your role or perspective
- Mention constraints (budget, timeline, audience)

**Use examples**:
- Show the AI what you want (few-shot prompting)
- Provide good and bad examples

**Structure your prompt**:
- Use headers, lists, and clear sections
- Separate instructions from content

**Iterate**:
- First response not perfect? Refine your prompt
- Learn what works for different model types

---

### Using Conversation History

**Multi-turn conversations**:
- AI remembers earlier messages in the same conversation
- Build on previous responses
- Refine answers incrementally

**Managing context**:
- Don't let conversations get too long (context window limits)
- Summarize key points periodically
- Start new conversations for unrelated topics

---

### Combining Models

**Use different models for different tasks**:
- Cheap model for drafts → Premium model for refinement
- Fast model for Q&A → Reasoning model for complex analysis
- Standard model for text → Vision model for images

**Workflow example**:
1. Use a budget-tier model to brainstorm ideas (cheap, fast)
2. Use a mid-tier model to write detailed content (balanced quality/cost)
3. Use a reasoning model to review and critique (deep analysis)

**Check leaderboards for each task**:
- Find the best coding model for step 1
- Find the best writing model for step 2
- Find the best reasoning model for step 3

---

## Privacy and Data Retention

**All models in KeystoneAgentic have Zero Data Retention (ZDR)**:
- Providers do not store your prompts
- Providers do not use your data for training
- Your conversations are immediately discarded after processing

[Learn more about Zero Data Retention](../security/zero-data-retention.md)

---

## Staying Current

### How to Keep Up with AI Progress

**Follow leaderboards**:
- Bookmark the leaderboards listed above
- Check monthly (or weekly for cutting-edge use cases)
- Pay attention to new model releases

**Join AI communities**:
- Reddit: r/MachineLearning, r/LocalLLaMA
- Twitter/X: Follow AI researchers and labs
- Discord: Join AI-focused communities

**Read industry news**:
- AI research papers (arXiv.org)
- AI newsletters and blogs
- Model release announcements

**Experiment regularly**:
- Test new models as they appear in KeystoneAgentic
- Compare performance on your specific use cases
- Don't assume yesterday's best model is still best today

---

## Next Steps

- **[Model Discovery](model-discovery.md)** - Browse and filter available models
- **[Model Management](model-management.md)** - Sync, activate, and configure models
- **[Chat Parameters (Coming Soon)** - Control temperature, tokens, and more
- **[Zero Data Retention](../security/zero-data-retention.md)** - Understand data privacy

---

## Further Learning

**Model Leaderboards** (check regularly):
- [LM Arena](https://lmarena.ai/leaderboard/)
- [OpenRouter Rankings](https://openrouter.ai/rankings)
- [Vellum LLM Leaderboard](https://www.vellum.ai/llm-leaderboard)
- [Artificial Analysis](https://artificialanalysis.ai/leaderboards/models)
- [Scale AI Leaderboard](https://scale.com/leaderboard)

**General AI Resources**:
- [Hugging Face Model Hub](https://huggingface.co/models)
- [Papers with Code Leaderboards](https://paperswithcode.com/sota)

Understanding LLMs empowers you to choose the right tool for every task—and adapt as the field evolves.

[← Back to Main Documentation](../README.md)
