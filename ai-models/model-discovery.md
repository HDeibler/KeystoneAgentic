# Model Discovery

The Model Discovery page is where you browse, filter, and sync AI models to your organization. This guide shows you how to find the perfect models for your needs.

---

## Accessing Model Discovery

1. Navigate to **Models** in the sidebar
2. You'll land on the **Model Discovery** tab by default
3. Browse hundreds of available AI models, all with Zero Data Retention

---

## Model Card Overview

Each model is displayed as a card showing key information:

### Model Name and Provider
- **Model Name**: The official identifier (e.g., displayed with version info)
- **Provider**: Which AI company created the model
- **Badge Indicators**: Visual tags for special features

### Description
- **What the model does**: Brief summary of capabilities
- **Expandable**: Click "Show more" to read full description
- **Markdown support**: Formatted text with links and highlights

### Context Window
- **Token

 limit**: Maximum input + output tokens
- **Real-world equivalent**: Approximate word count
- **Examples**:
  - 8K tokens ≈ 6,000 words
  - 128K tokens ≈ 96,000 words
  - 1M tokens ≈ 750,000 words

### Pricing
- **Input cost**: Price per 1M input tokens
- **Output cost**: Price per 1M output tokens
- **Total cost estimate**: Combined pricing indicator
- **Color coding**: Green (cheap), yellow (moderate), red (expensive)

### Uptime Statistics
- **Last 30 minutes**: Real-time reliability data
- **Percentage**: Model availability
- **Status indicator**: Green (good), yellow (degraded), red (down)

### Features and Capabilities
Visual badges showing what the model can do:
- **Streaming**: Real-time word-by-word responses
- **Function Calling**: Can use external tools and APIs
- **Vision**: Can analyze images
- **Reasoning**: Chain-of-thought thinking
- **Additional features**: Displayed as capability tags

### Sync Button
- **Sync**: Add this model to your organization
- **Synced**: Already added (button disabled)
- **Quick action**: One-click to make the model available

---

## Browsing Models

### Default View
- Models are displayed in a grid layout
- 50 models per page
- Sorted by relevance or popularity

### Pagination
- **Page controls**: Navigate between pages at the bottom
- **Results counter**: Shows "Showing X-Y of Z models"
- **Previous / Next**: Arrow buttons to move between pages

---

## Filtering Models

Use powerful filters to narrow down your search:

### Search Bar
**Location**: Top of the page

**What you can search**:
- Model name or ID
- Provider name
- Keywords in description
- Capabilities

**How it works**:
- Type your query and press Enter
- Results update instantly (client-side filtering)
- Clears when you delete the search text

**Examples**:
- "vision" - Find models with image analysis
- "reasoning" - Find thinking models
- "coding" - Find code-specialized models

---

### Provider Filter
**Filter by AI company**:
- Dropdown showing all available providers
- Select one or "All Providers"
- Instantly filters the catalog

**Use case**: If you prefer models from a specific provider or want to compare their offerings

---

### Context Window Filter
**Set minimum and maximum token limits**:
- **Min Context**: Minimum context window size
- **Max Context**: Maximum context window size
- **Slider or input**: Enter values directly

**Use case**:
- Need to process long documents? Set min to 128K+
- Want fast, cheap models? Set max to 32K

---

### Capabilities Filter
**Multi-select for specific features**:
- **Streaming**: Real-time responses
- **Function Calling**: Tool usage
- **Vision**: Image analysis
- **Reasoning**: Chain-of-thought
- **And more**: Additional model capabilities

**How it works**:
- Check the capabilities you need
- Models must have ALL selected capabilities
- Uncheck to remove filter

**Use case**: Need vision + streaming? Select both to find compatible models.

---

### Price Filter
**Set maximum cost threshold**:
- **Slider**: Adjust maximum price per 1M tokens
- **Range**: $0 to $60+ per 1M tokens
- **Filters both input and output**: Uses combined pricing

**Use case**: Budget-conscious? Set a max price to see only affordable models.

---

### Uptime Filter
**Set minimum reliability threshold**:
- **Slider**: Minimum uptime percentage
- **Range**: 0% to 100%
- **Based on last 30 minutes**: Real-time data

**Use case**: Mission-critical applications? Set min uptime to 95%+ to see only reliable models.

---

### Tag Filter (Coming Soon)
**Filter by model categories**:
- Tags like "coding", "creative", "multilingual"
- Multi-select for combined filtering
- Community-driven or provider-assigned tags

---

### Active Filters Display
- **Filter chips**: Visual indicators of active filters
- **Clear individual**: Click X on a chip to remove that filter
- **Clear all**: Button to reset all filters at once
- **Active count**: "3 filters active" indicator

---

## Understanding Model Rankings

### How to Choose

Models aren't ranked within KeystoneAgentic—instead, use external leaderboards to compare:

**Recommended leaderboards**:
- [LM Arena](https://lmarena.ai/leaderboard/) - Community preferences
- [OpenRouter Rankings](https://openrouter.ai/rankings) - Performance metrics
- [Vellum LLM Leaderboard](https://www.vellum.ai/llm-leaderboard) - Task-specific benchmarks
- [Artificial Analysis](https://artificialanalysis.ai/leaderboards/models) - Cost vs. quality
- [Scale AI Leaderboard](https://scale.com/leaderboard) - Academic benchmarks

**Why external leaderboards?**
- Rankings change constantly (weekly or monthly)
- AI progress is exponential
- What's "best" depends on your specific use case
- Leaderboards are updated in real-time as models improve

[Learn more about using leaderboards](/docs/ai-models/understanding-llms#finding-the-best-models)

---

## Syncing Models

### How to Sync

1. Find a model you want to use
2. Click the **Sync** button on the model card
3. Model is instantly added to your organization
4. Success message confirms the sync
5. Button changes to **Synced** (disabled)

### What Happens When You Sync

- **Model added**: Appears in your "Synced Models" tab
- **Immediately available**: Can be used in conversations right away
- **Organization-wide**: All team members can use it
- **No limits**: Sync as many models as you want

### Who Can Sync Models

- **Admins**: Yes
- **Members**: Yes
- **Viewers**: No (read-only access)

[See role permissions](/docs/organization/roles-permissions)

---

## Batch Syncing (Coming Soon)

Future feature to sync multiple models at once:
- **Select multiple**: Checkboxes on model cards
- **Batch sync**: One button to sync all selected
- **Smart recommendations**: Suggested model bundles

---

## Model Details

### Expanding Descriptions
- Click **Show more** to read full model description
- Click **Show less** to collapse
- Descriptions include:
  - Strengths and ideal use cases
  - Special features
  - Training details (when available)
  - Provider notes

### Viewing Full Specifications
Click on a model card (future feature) to see:
- Complete capability list
- Detailed pricing breakdown
- Historical uptime data
- Version information
- Release notes

---

## Tips for Effective Discovery

### Start Broad, Then Filter
1. Browse without filters to see what's available
2. Notice patterns in pricing, capabilities, providers
3. Apply filters to narrow down
4. Compare similar models using leaderboards

### Sync Multiple Models
- Don't rely on a single model
- Sync 3-5 models covering different use cases:
  - One fast, cheap model for simple tasks
  - One balanced model for general use
  - One premium model for complex tasks
  - Backups in case of downtime

### Test Before Committing
- Sync a model and try it in conversations
- Compare responses across models
- Check actual performance vs. specifications
- Keep the ones that work best for you

### Monitor New Releases
- Check the Model Discovery page regularly
- New models appear as they're released
- AI evolves rapidly—yesterday's best may be surpassed today
- Experiment with new models as they arrive

---

## Understanding Model Metadata

### Model Versioning
Some models include version numbers in their names:
- Indicates updates or improvements
- Higher versions may have better performance
- Check release notes for changes

### Context Window Sizes
Why different sizes matter:
- **Small (4K-8K)**: Fast, cheap, good for short conversations
- **Medium (16K-32K)**: Balanced, handles multi-turn dialogue
- **Large (128K-200K)**: Can process entire documents
- **Extra Large (1M+)**: Experimental, massive analysis

### Pricing Dynamics
- **Input vs. Output**: Output usually costs more
- **Reasoning premium**: Thinking models cost 2-5x more
- **Smaller = cheaper**: Lower parameter models cost less
- **Check leaderboards**: Find best value for quality

---

## Troubleshooting

### No Models Showing
**Possible causes**:
- Filters too restrictive
- Search query too specific
- Network issue loading catalog

**Solutions**:
- Click "Clear all filters"
- Refresh the page
- Check your internet connection

---

### Can't Sync a Model
**Possible causes**:
- Already synced (button says "Synced")
- You're a Viewer (no sync permissions)
- Network error

**Solutions**:
- Check if it's in your "Synced Models" tab
- Verify your role (ask Admin for Member access)
- Try again or refresh the page

---

### Model Showing Low Uptime
**What it means**: Model is experiencing downtime or degraded performance

**What to do**:
- Sync an alternative model as backup
- Check again later (uptime updates every 30 minutes)
- Use a different model for critical tasks

---

### Pricing Seems High
**Context**:
- Prices are per 1M tokens, not per conversation
- 1M tokens ≈ 750K words
- Most conversations use 100-10K tokens

**Example**:
- Model costs $5 per 1M tokens
- Your conversation uses 1,000 tokens (750 words)
- Cost: $0.005 (half a cent)

**Use price filter** to find budget models if needed.

---

## Best Practices

### Discovery Workflow
1. **Start with leaderboards**: Identify top performers for your use case
2. **Filter in KeystoneAgentic**: Apply filters matching your requirements
3. **Sync candidates**: Add 3-5 models that look promising
4. **Test in practice**: Use them in real conversations
5. **Refine selection**: Keep the best, remove underperformers

### Regular Review
- **Monthly**: Check for new models
- **Quarterly**: Review your synced models and remove unused ones
- **After major releases**: Test new state-of-the-art models

### Cost Optimization
- Use price filter to identify budget options
- Test cheap models first before committing to expensive ones
- Check leaderboards for "best value" rankings
- Monitor your organization's usage to optimize model selection

---

## Next Steps

- **[Sync Your First Model](/docs/ai-models/model-discovery#syncing-models)** - Add a model to your organization
- **[Manage Synced Models](/docs/ai-models/model-management)** - Activate, deactivate, and configure models
- **[Understanding LLMs](/docs/ai-models/understanding-llms)** - Learn about tokens, context windows, and capabilities
- **[Chat Parameters (Coming Soon)** - Control temperature and other settings

---

**Explore, experiment, and find the perfect models for your needs.**
