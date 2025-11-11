# Usage Tracking & Analytics

Monitor your organization's AI usage, track token consumption, and optimize costs with KeystoneAgentic's analytics dashboard. This guide shows you how to understand and leverage usage data.

---

## Accessing Analytics

### Dashboard Overview (All Roles)

**Location**: Main Dashboard page

**What you see**:
- User seats (current/total)
- Monthly tokens (used/allocated)
- Requests this month
- Active conversations

**Available to**: All users (Admin, Member, Viewer)

---

### Detailed Analytics (Admin Only)

**Location**: Navigate to **Analytics** in the sidebar

**What you see**:
- Comprehensive usage breakdowns
- Per-user analytics
- Per-model analytics
- Date range filtering
- Exportable reports (coming soon)

**Available to**: Admins only

[Learn more about roles](/docs/organization/roles-permissions)

---

## Dashboard Metrics

### User Seats

**Shows**: Current members vs. plan limit

**Example**: "3 / 5 seats"
- **3**: Active users in your organization
- **5**: Maximum allowed by your plan

**Color coding**:
- Green: Under 80% utilization
- Yellow: 80-100% utilization
- Red: At limit (can't invite more users)

**Action**: Upgrade plan if you need more seats

---

### Monthly Tokens

**Shows**: Token consumption vs. monthly quota

**Example**: "245,000 / 500,000 tokens (49%)"
- **245,000**: Tokens used this month
- **500,000**: Your monthly allocation
- **49%**: Percentage used

**Color coding**:
- Green: Under 80% usage
- Yellow: 80-100% usage
- Red: Over 100% (grace period up to 110%)

**What happens at quota limits**:
- **80%**: Warning notification
- **100%**: Hard limit, new requests blocked
- **110%**: Grace period expires, strict enforcement

**Action**: Monitor closely and upgrade if consistently hitting limits

---

### Requests This Month

**Shows**: Total AI requests made

**What counts as a request**:
- Each message sent to an AI model
- RAG queries (document retrieval + generation)
- API calls (when available)

**Use case**: Understand overall platform usage

---

### Active Conversations

**Shows**: Ongoing chat sessions

**What it means**:
- Conversations started but not archived
- Recently active discussions
- Open threads

**Use case**: Track engagement and collaboration

---

## Detailed Analytics (Admin)

### Overall Metrics

**Total Conversations**:
- All-time conversation count
- New conversations this month
- Trend vs. previous month

**Total Messages**:
- All messages sent to AI
- Average messages per conversation
- Most active days/hours

**Total Tokens Used**:
- Lifetime token consumption
- This month's usage
- Projected usage (if trend continues)

**Total Documents Uploaded**:
- Knowledge base size
- Documents per user
- Storage utilization

---

### User Analytics

**Per-user breakdown showing**:
- **Name and Email**: Who is using the platform
- **Tokens Used**: Individual consumption
- **Conversations**: Number of chats started
- **Messages Sent**: Total messages
- **Documents Uploaded**: Knowledge base contributions
- **Avg Docs per Message**: Document usage in RAG
- **Avg Conversation Length**: Messages per conversation
- **Model Usage**: Which models they prefer

### Sorting and Filtering

**Sort by**:
- Tokens used (highest to lowest)
- Conversations (most active users)
- Messages (chattiest users)
- Documents (knowledge contributors)

**Filter by**:
- Minimum tokens used
- Minimum conversations
- Date range

**Use case**: Identify power users, optimize training, allocate resources

---

### Model Analytics

**Per-model breakdown showing**:
- **Model Name**: Which AI model
- **Conversations**: How many times used
- **Tokens Consumed**: Total tokens for this model
- **Tool Calls**: Function calling usage
- **Flagged Messages**: Moderation or quality issues
- **Avg Response Length**: Typical output size

### Model Comparison

**Use case**: Understand which models are:
- Most cost-effective
- Most frequently used
- Best for specific tasks
- Underutilized (consider removing)

**Optimization strategies**:
- Replace expensive, high-volume models with cheaper alternatives
- Promote high-quality, low-cost models to team
- Deactivate unused models

---

## Date Range Filtering

**Select custom ranges**:
- Last 7 days
- Last 30 days
- This month
- Last month
- Custom date range

**Apply to**:
- Overall metrics
- User analytics
- Model analytics

**Use case**: Compare periods, identify trends, track growth

---

## Quota Management

### Understanding Your Quota

**Monthly allocation**: Based on your plan
- Trial: 100,000 tokens/month
- Starter: 500,000 tokens/month
- Professional: 2,000,000 tokens/month
- Enterprise: 10,000,000 tokens/month

**Reset schedule**: Quotas reset on your subscription anniversary date

**Example**:
- Subscription started: January 15
- Quota resets: 15th of every month

---

### Monitoring Usage

**Track progress**:
- Check dashboard daily during high-usage periods
- Review detailed analytics weekly
- Plan upgrades before hitting 80%

**Warning thresholds**:
- 80%: Email notification
- 90%: Warning in dashboard
- 100%: Requests blocked, grace period begins
- 110%: Grace period expires

---

### What Happens at Quota Limit

**At 100% usage**:
- New AI requests are blocked
- Existing conversations can be viewed (but not continued)
- Grace period allows up to 110% (temporary buffer)
- Notification sent to all Admins

**Actions you can take**:
1. **Upgrade plan**: Increase monthly quota immediately
2. **Wait for reset**: Quotas reset monthly
3. **Optimize usage**: Use cheaper models, shorten prompts

---

## Usage Optimization

### Cost-Saving Strategies

**Use cheaper models for simple tasks**:
- Drafts, brainstorming → Budget models
- Final output, complex reasoning → Premium models
- Check leaderboards for best value models

**Shorten prompts**:
- Remove unnecessary context
- Be concise in your questions
- Avoid repeating information

**Limit conversation history**:
- Start new conversations for unrelated topics
- Long conversations send more context (more tokens)
- Summarize and restart if conversations get long

**Optimize RAG usage**:
- Upload well-organized documents (better retrieval = fewer tokens)
- Use specific queries to retrieve fewer chunks
- Remove duplicate or redundant documents

---

### Identifying High-Usage Users

**In User Analytics**:
- Sort by "Tokens Used"
- Identify users with disproportionate consumption
- Reach out for training or optimization tips

**Possible causes of high usage**:
- Using expensive models unnecessarily
- Long, repetitive conversations
- Inefficient prompting
- Legitimate high-volume use case

**Solutions**:
- Train users on cost-effective practices
- Suggest model alternatives
- Provide prompt engineering guidance

---

### Model Performance Tracking

**In Model Analytics**:
- Identify models with high token usage
- Compare cost vs. quality
- Look for underused models (consider deactivating)

**Questions to ask**:
- Is this expensive model worth the cost?
- Can we achieve similar quality with a cheaper model?
- Are we using the right model for each task?

---

## Reporting (Coming Soon)

Future analytics features:

### Exportable Reports
- Download analytics as CSV or PDF
- Schedule automated reports (weekly/monthly)
- Email reports to stakeholders

### Custom Dashboards
- Create custom views for specific metrics
- Save favorite filters
- Pin important charts

### Predictive Analytics
- Forecast usage based on trends
- Predict when quota will be exceeded
- Suggest plan upgrades proactively

### Cost Breakdown
- Detailed cost per user
- Cost per model
- ROI calculations

---

## Privacy and Data Access

### Who Can See What

**All Users (Admin, Member, Viewer)**:
- Own usage statistics
- Overall organization metrics (dashboard)
- Aggregated data (no individual breakdowns)

**Admins Only**:
- Detailed per-user analytics
- Detailed per-model analytics
- Individual usage patterns
- Full analytics dashboard

### Data Retention

**Analytics data is retained**:
- Indefinitely for aggregated metrics
- 90 days for detailed logs
- Can be exported before deletion

**User privacy**:
- Admins can see usage but not conversation content (unless they open conversations)
- Analytics track metadata (tokens, timestamps) not message content

---

## Troubleshooting

### Analytics Not Updating
**Cause**: Data refreshes every 60 seconds

**Solution**: Wait a minute and refresh the page

---

### Numbers Don't Match Expectations
**Possible causes**:
- Tokens include both input and output
- Conversation history counts toward tokens
- RAG adds document chunks to token count

**Solution**: Review token calculation in [Understanding LLMs](/docs/ai-models/understanding-llms#tokens)

---

### Can't Access Analytics Page
**Cause**: You're a Member or Viewer (not Admin)

**Solution**: Ask an Admin for access, or request Admin role if appropriate

---

### Quota Exceeded Unexpectedly
**Cause**: Sudden spike in usage

**Solution**:
- Check User Analytics to identify high usage
- Review recent activity
- Upgrade plan if needed

---

## Best Practices

### Regular Monitoring

**Daily** (during high-usage periods):
- Check dashboard metrics
- Monitor quota percentage
- Watch for anomalies

**Weekly**:
- Review user analytics
- Identify trends
- Optimize model usage

**Monthly**:
- Full analytics review
- Compare to previous months
- Plan capacity for next month

---

### Proactive Management

**Set internal thresholds**:
- Alert team at 50% quota usage
- Review usage at 75%
- Plan upgrade at 80%

**Don't wait for quota limits**—manage proactively.

---

### Team Education

**Share analytics with your team**:
- Show cost impact of model choices
- Teach optimization techniques
- Celebrate efficient users

**Create guidelines**:
- Which models for which tasks
- Prompt engineering best practices
- When to use RAG vs. direct prompts

---

## Next Steps

- **[Understanding LLMs](/docs/ai-models/understanding-llms)** - Learn about tokens and costs
- **[Model Management](/docs/ai-models/model-management)** - Optimize your model selection
- **[Organization Settings (Admin feature - Coming Soon)** - Manage quotas and billing

---

**Track, optimize, and scale your AI usage with confidence.**
