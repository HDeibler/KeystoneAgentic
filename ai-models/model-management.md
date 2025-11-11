# Model Management

Once you've synced models to your organization, use the Model Management page to activate, deactivate, configure, and organize them. This guide shows you how to manage your model library.

---

## Accessing Synced Models

1. Navigate to **Models** in the sidebar
2. Click the **Synced Models** tab
3. View all models you've added to your organization

---

## Synced Models Overview

### What You'll See

**Model List**:
- All models currently synced to your organization
- Same information as discovery (name, provider, pricing, context window)
- Additional management controls

**Model Status**:
- **Active**: Model is available for use in conversations
- **Inactive**: Model is synced but not available for use

**Default Model Indicator**:
- Badge showing which model is the organization default
- Used as the fallback when no specific model is selected

---

## Activating and Deactivating Models

### Why Control Model Status?

**Activate models** to make them available for use:
- Team members can select them in conversations
- Appears in model selection dropdowns
- Included in organization's active model count

**Deactivate models** to hide them without deleting:
- Temporarily remove from selection
- Preserve configuration and settings
- Can reactivate anytime without re-syncing

### How to Activate a Model

1. Find the inactive model in your synced list
2. Click the **Activate** button
3. Model status changes to "Active"
4. Now available for conversations

### How to Deactivate a Model

1. Find the active model in your synced list
2. Click the **Deactivate** button
3. Confirm deactivation if prompted
4. Model status changes to "Inactive"
5. No longer appears in conversation model selection

### Who Can Activate/Deactivate?

- **Admins**: Yes
- **Members**: Yes
- **Viewers**: No

[See role permissions](/docs/organization/roles-permissions)

---

## Setting a Default Model

### What is the Default Model?

The **default model** is used when:
- Starting a new conversation without selecting a model
- A conversation's model is deactivated or removed
- Fallback for API requests without model specification

### How to Set Default

1. Find the model you want as default
2. Click **Set as Default**
3. A badge appears: "Default"
4. Previous default loses the badge

### Choosing the Right Default

**Consider**:
- **Cost**: Will be used frequently, choose affordable option
- **Performance**: Should handle general tasks well
- **Availability**: Select a model with high uptime
- **Balance**: Mid-tier models make good defaults

**Examples of good defaults**:
- Fast, reliable models with 32K-128K context
- Mid-tier pricing ($1-5 per 1M tokens)
- Strong general-purpose performance
- High uptime (95%+)

**Check leaderboards** for well-rounded models suitable as defaults:
- [LM Arena](https://lmarena.ai/leaderboard/)
- [OpenRouter Rankings](https://openrouter.ai/rankings)

---

## Deleting Synced Models

### When to Delete

- Model is no longer needed
- You've found a better alternative
- Cleaning up unused models
- Model pricing has increased significantly

### How to Delete

1. Find the model in your synced list
2. Click **Delete** or trash icon
3. Confirm deletion in the dialog
4. Model is removed from your organization

**Important**: Deleting a model:
- Removes it from your synced models list
- Makes it unavailable in conversation selection
- Does NOT delete it from the discovery catalog (you can re-sync anytime)
- Does NOT affect existing conversations that used this model

### Preventing Accidental Deletion

**You cannot delete**:
- The default model (set another model as default first)
- A model currently in use (if conversations are active)

**Best practice**: Deactivate first, observe for a week, then delete if truly unused.

---

## Filtering and Searching Synced Models

### Search Bar
Type to search your synced models by:
- Model name
- Provider name
- Keywords

### Filter by Status
- **All Models**: Show active and inactive
- **Active Only**: Models currently available
- **Inactive Only**: Deactivated models

### Sort Options
Click column headers to sort by:
- **Name**: Alphabetical (A-Z or Z-A)
- **Provider**: Group by AI company
- **Context Window**: Smallest to largest
- **Price**: Cheapest to most expensive
- **Status**: Active first or inactive first

---

## Batch Actions (Coming Soon)

Future features for managing multiple models at once:

### Batch Activate/Deactivate
- Select multiple models with checkboxes
- Click "Activate Selected" or "Deactivate Selected"
- Apply status changes to all at once

### Batch Delete
- Select multiple models
- Click "Delete Selected"
- Confirm and remove all at once

### Organize by Collections
- Create model collections (e.g., "Coding Models", "Creative Models")
- Tag models for easy filtering
- Quick-switch between collections

---

## Model Configuration (Future Feature)

Coming soon: Per-model settings

### Custom Aliases
- Rename models for easier identification
- Example: "gpt-4-turbo-2024" → "Fast GPT-4"
- Organization-specific naming

### Default Parameters
- Set default temperature per model
- Configure max tokens
- Preset frequency/presence penalties
- Applied automatically when using the model

### Cost Limits
- Set spending caps per model
- Alert when approaching limit
- Auto-deactivate if limit exceeded

### Usage Tracking
- See token consumption per model
- Identify most-used models
- Optimize model selection based on data

---

## Monitoring Model Performance

### Uptime Tracking

**Real-time status**:
- Green: Operational
- Yellow: Degraded performance
- Red: Down or unavailable

**Last 30 minutes**:
- Percentage uptime
- Updates automatically

**What to do if a model is down**:
1. Switch to an alternative model
2. Check back later (status updates frequently)
3. If prolonged, remove from synced models and find replacement

### Model Availability Alerts (Coming Soon)

- Email or in-app notifications when synced models go down
- Suggested alternatives when downtime occurs
- Historical uptime reports

---

## Best Practices

### Sync Strategy

**Recommended approach**:
- **3-5 active models** covering different use cases
- **1-2 backups** for each category (in case of downtime)
- **Deactivate** rather than delete (easier to restore)

**Model categories to cover**:
- **Budget model**: Fast, cheap for simple tasks
- **Balanced model**: Good default for general use
- **Premium model**: High quality for complex tasks
- **Specialized model**: Vision, coding, or reasoning (if needed)

### Regular Maintenance

**Monthly review**:
- Check which models you actually use (via Analytics)
- Deactivate unused models
- Delete models you haven't used in 90+ days
- Sync new models that rank well on leaderboards

**After major AI releases**:
- Test new state-of-the-art models
- Compare to your current defaults
- Update default if newer model outperforms

### Cost Management

**Monitor spending**:
- Use Analytics to see per-model token usage
- Identify expensive models consuming high volumes
- Consider cheaper alternatives for high-volume tasks

**Optimize model selection**:
- Use cheap models for drafts
- Use premium models for final outputs
- Don't over-use reasoning models for simple tasks

---

## Model Lifecycle

### Syncing
1. Discover model in catalog
2. Click "Sync"
3. Model added to organization

### Activation
4. Activate model to make it available
5. Optionally set as default

### Usage
6. Use in conversations
7. Monitor performance and cost

### Maintenance
8. Review usage periodically
9. Deactivate if not needed
10. Delete if permanently unused

### Replacement
11. Sync better alternatives
12. Set new default
13. Remove old model

---

## Troubleshooting

### Can't Activate a Model
**Possible causes**:
- Already active
- You're a Viewer (no permissions)

**Solutions**:
- Check status column
- Ask Admin for Member role

---

### Can't Set as Default
**Possible causes**:
- Model is inactive
- You're a Viewer

**Solutions**:
- Activate the model first
- Ask Admin or Member to set it

---

### Can't Delete a Model
**Possible causes**:
- It's the default model
- It's currently in use in active conversations

**Solutions**:
- Set a different model as default first
- Wait for active conversations to end
- Deactivate instead of deleting

---

### Model Disappeared from Synced List
**Possible causes**:
- Another user deleted it
- Model lost ZDR status and was auto-removed

**Solutions**:
- Check with team members
- Re-sync from discovery if available
- Choose an alternative model

---

### Model Showing as Down
**What it means**: Temporary provider outage

**What to do**:
- Use an alternative active model
- Check again in 30 minutes
- If prolonged (24+ hours), consider removing

---

## Understanding Model Metadata

### Provider Information
- Shows which AI company created the model
- Some providers have multiple models
- Provider reputation and reliability varies

### Version Numbers
- Models may include version/date in name
- Newer versions often improve on older ones
- Check release notes for changes

### Feature Badges
Visual indicators of capabilities:
- **Streaming**: Real-time responses
- **Vision**: Image analysis
- **Reasoning**: Chain-of-thought
- **Function Calling**: Tool usage

---

## Synced Models vs. Discovery

### Discovery Tab
- **Purpose**: Browse all available models
- **Action**: Sync models to your organization
- **Scope**: Hundreds of models

### Synced Models Tab
- **Purpose**: Manage your organization's models
- **Action**: Activate, deactivate, configure, delete
- **Scope**: Only models you've synced

**Workflow**:
1. Discover → Sync
2. Synced Models → Activate and configure
3. Conversations → Use models

---

## API and Programmatic Access (Coming Soon)

Future capabilities:

### API Key Model Access
- Generate API keys with model restrictions
- Limit which models can be accessed via API
- Track API usage per model

### Model Selection via API
- Specify model in API requests
- Fallback to default if not specified
- Override default on per-request basis

---

## Next Steps

- **[Understanding LLMs](/docs/ai-models/understanding-llms)** - Learn about model types and capabilities
- **[Model Discovery](/docs/ai-models/model-discovery)** - Find and sync new models
- **[Chat Parameters (Coming Soon)** - Control temperature and other settings
- **[Analytics (Coming Soon)** - Track model usage and costs

---

**Effective model management ensures you always have the right tool for every task.**
