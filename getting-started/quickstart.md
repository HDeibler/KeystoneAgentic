# Quick Start Guide

[← Back to Main Documentation](../README.md)

Get up and running with KeystoneAgentic in minutes. This guide walks you through the essential steps to start using AI-powered conversations with your team.

---

## What is KeystoneAgentic?

KeystoneAgentic is your **unified AI platform** that provides:

| Feature | Benefit |
|:--------|:--------|
| **Multi-Model Access** | Connect to 200+ AI models from leading providers |
| **Zero Data Retention** | Every model guarantees your data is never stored or used for training |
| **Knowledge Base & RAG** | Upload documents and AI references them automatically |
| **Team Collaboration** | Role-based access control for secure team usage |
| **Usage Analytics** | Track token consumption and optimize costs |

---

## Getting Started in 5 Steps

### Step 1: Create Your Account

**Navigate to the signup page**

1. Choose your **organization name** (this becomes your unique identifier)
2. Enter your **email address**
3. Create a **secure password**
4. Click **Create Account**

**What you get:**
- 14-day free trial
- 100,000 tokens to start
- Access to all features
- Up to 5 team members included

**No credit card required** for the trial period.

---

### Step 2: Sync Your First AI Model

Once logged in, you'll need at least one AI model to start chatting.

**Navigate to:** Models → Discover Tab

**Quick sync options:**

<details>
<summary><strong>For General Use (Recommended)</strong></summary>

**Sync a balanced model:**
- Look for models with 16K-32K context window
- Mid-tier pricing ($2-5 per 1M tokens)
- "Streaming" capability enabled
- High uptime (>95%)

**Examples:** GPT-3.5 Turbo, Claude 3 Haiku, or similar mid-tier models

</details>

<details>
<summary><strong>For Document Analysis</strong></summary>

**Sync a large-context model:**
- Context window of 128K+ tokens
- Ability to process entire documents
- RAG-compatible

**Examples:** Claude 3.5 Sonnet, GPT-4 Turbo (128K), or similar large-context models

</details>

<details>
<summary><strong>For Budget-Conscious Users</strong></summary>

**Sync an economical model:**
- Lower cost per 1M tokens ($0.10-$1)
- Fast response times
- Good for high-volume, simple tasks

**Examples:** Smaller parameter models, check leaderboards for best value

</details>

**How to sync:**
1. Find a model that matches your needs
2. Click **"Sync"** on the model card
3. Model appears in "Synced Models" tab
4. Now ready to use in conversations

**Pro Tip:** Sync 2-3 models so you can compare quality and switch if one is down

[Learn more about choosing models →](../ai-models/model-discovery.md)

---

### Step 3: Start Your First Conversation

**Navigate to:** Chat page (sidebar)

**Using the chat interface:**

1. **Select a model** from the dropdown at the top
2. **Type your message** in the text box at the bottom
3. **Press Enter** or click Send
4. **Watch the response** stream in real-time

**Your first conversation is that simple.**

#### Chat Features You'll See:

**Message History**
- All messages display in chronological order
- Your messages on the right
- AI responses on the left
- Conversation persists until you start a new one

**Model Switching**
- Change models mid-conversation using the dropdown
- Each message shows which model generated it
- Try different models for the same question to compare

**Streaming Responses**
- Compatible models show responses word-by-word
- See progress immediately
- Stop generation if needed

---

### Step 4: Upload Documents (Optional but Powerful)

Give your AI access to your specific information through document upload.

**Navigate to:** Knowledge Base → Documents

**Upload process:**

1. Click **"Upload Document"** button
2. Choose a file:
   - **PDF** - Best for formatted documents
   - **DOCX** - Microsoft Word files
   - **TXT** - Plain text files
   - **MD** - Markdown documentation
3. File uploads and processes automatically (10-60 seconds)
4. Status changes from "Processing" to "Ready"
5. Documents now available for RAG in conversations

**What happens when you upload:**
- Text is extracted from your document
- Content is broken into searchable chunks
- AI can find and reference relevant sections when you chat

**Using documents in chat:**
The system automatically searches your documents when questions seem relevant to uploaded content. The AI will reference your documents in its responses, providing grounded, accurate answers based on YOUR information.

[Learn more about document management →](../knowledge-base/document-management.md)

---

### Step 5: Invite Your Team

Share KeystoneAgentic with your colleagues.

**Navigate to:** Settings → Organization → Members

**Invitation process:**

1. Click **"Invite Member"** button
2. Enter team member's **email address**
3. Assign a **role**:
   - **Admin** - Full access including billing and team management
   - **Member** - Use models, upload documents, manage conversations
   - **Viewer** - Read-only access to view but not edit
4. Click **"Send Invite"**
5. They receive an email with signup link

**Team members can:**
- Use all synced models
- Access shared documents
- Collaborate on knowledge base
- View their own usage statistics

**Admins can:**
- Everything Members can do, plus:
- Manage team member roles
- View organization-wide analytics
- Manage billing and subscription
- Configure organization settings

[Learn more about roles and permissions →](../organization/roles-permissions.md)

---

## Understanding Your Dashboard

After logging in, your **Dashboard** shows:

### Usage Overview
- **Token consumption** for current billing period
- **Remaining quota** based on your plan
- **Usage trend** over time
- **Alert indicators** when approaching limits

### Quick Actions
- Start new conversation
- Upload documents
- Discover models
- Invite team members

### Recent Activity
- Latest conversations
- Recently uploaded documents
- Team member activity
- Model usage statistics

---

## Key Concepts to Know

### Tokens

> **Tokens** are pieces of text the AI processes. Roughly 1 token ≈ 0.75 words.

**Why they matter:**
- Pricing is based on tokens used
- Your plan includes a monthly token quota
- Both input (what you send) and output (AI generates) count

**Typical usage:**
- Simple question + answer: 100-500 tokens
- Long conversation: 2,000-5,000 tokens
- Document analysis: 5,000-20,000 tokens

**Your 100K trial tokens** = approximately:
- 200 simple conversations, OR
- 20-30 document analysis tasks, OR
- 50 standard multi-turn conversations

[Learn more about tokens →](../ai-models/understanding-llms.md#tokens)

---

### Context Window

> **Context window** = maximum text an AI can process at once (input + output combined)

**Model context sizes:**
- **8K tokens** - ~6,000 words - Short conversations
- **32K tokens** - ~24,000 words - Extended conversations
- **128K tokens** - ~96,000 words - Full document analysis
- **1M+ tokens** - ~750,000 words - Massive documents

**What fits in the context:**
- Your current message
- Conversation history
- Retrieved document chunks (RAG)
- System instructions
- AI's response

**When context is full:**
- Older messages drop from conversation
- AI "forgets" early parts of discussion
- Start a new conversation if needed

[Learn more about context windows →](../ai-models/understanding-llms.md#context-window)

---

### RAG (Retrieval-Augmented Generation)

> **RAG** = AI + Your Documents working together

**How it works:**
1. You ask a question
2. System searches your uploaded documents
3. Most relevant sections are retrieved
4. AI uses those sections to answer accurately
5. Response is grounded in YOUR specific information

**Benefits:**
- Accurate answers based on your documents
- No hallucinations about your specific data
- AI references exact sources
- Keep information current by updating documents

[Learn more about RAG →](../knowledge-base/rag-overview.md)

---

### Zero Data Retention (ZDR)

> **Every model in KeystoneAgentic has Zero Data Retention**

**What this means:**
- Your prompts are processed and immediately discarded
- AI providers don't store your conversations
- Your data never trains AI models
- Complete privacy for sensitive information

**You're protected:**
- Proprietary business information
- Customer data
- Confidential strategy discussions
- Personal or sensitive content

[Learn more about Zero Data Retention →](../security/zero-data-retention.md)

---

## Subscription Plans

### Trial - Free for 14 Days
- **Tokens:** 100,000
- **Users:** Up to 5
- **Features:** Everything included
- **No credit card** required

### Starter - $29/month
- **Tokens:** 500,000/month
- **Users:** Up to 5
- **Storage:** 1 GB documents
- **Support:** Email support

### Professional - $99/month
- **Tokens:** 2,000,000/month
- **Users:** Up to 20
- **Storage:** 10 GB documents
- **Support:** Priority support

### Enterprise - $499/month
- **Tokens:** 10,000,000/month
- **Users:** Unlimited
- **Storage:** 100 GB documents
- **Support:** Dedicated support + SLA

**All plans include:**
- Access to all available models
- Zero Data Retention on all models
- RAG and knowledge base
- Team collaboration features
- Usage analytics

---

## Tips for Getting the Most Value

### Writing Better Prompts

**Be specific:**
```
❌ Vague: "Tell me about marketing"
✅ Specific: "List 5 digital marketing strategies for B2B SaaS"
```

**Provide context:**
```
❌ No context: "Write an email"
✅ With context: "Write a professional email to a client explaining a 2-week project delay, maintaining positive tone"
```

**Use examples:**
```
Show the AI what format you want by providing an example first, then asking it to generate similar content.
```

[Learn more about effective prompting →](../ai-models/understanding-llms.md#writing-effective-prompts)

---

### Organizing Your Knowledge Base

**Good document preparation:**
- Use descriptive filenames
- Structure with clear headings
- Keep documents focused on single topics
- Remove outdated information regularly
- Include version dates in filenames

**Document organization:**
```
✅ Good: Employee_Handbook_2024_v2.pdf
✅ Good: API_Documentation_Authentication.md
✅ Good: Sales_Process_Q1_2024.docx

❌ Poor: document1.pdf
❌ Poor: final_FINAL_v2.docx
❌ Poor: untitled.txt
```

[Learn more about document best practices →](../knowledge-base/document-management.md)

---

### Choosing the Right Model

**Match model to task:**

| Task Type | Model Recommendation |
|-----------|---------------------|
| Quick Q&A | Fast, economical models |
| Content writing | Balanced mid-tier models |
| Complex analysis | Reasoning models (slower, pricier) |
| Long documents | Large context window models (128K+) |
| Image analysis | Vision-capable models |
| Code generation | Code-specialized models |

**Cost optimization:**
- Use cheaper models for high-volume simple tasks
- Reserve expensive models for complex work
- Test with budget models before committing to premium
- Monitor usage to identify cost savings

[Learn more about choosing models →](../ai-models/understanding-llms.md#choosing-the-right-model)

---

## Common Questions

### How do I know which model to use?

Check these resources:
- **Leaderboards:** [LM Arena](https://lmarena.ai/leaderboard/), [OpenRouter Rankings](https://openrouter.ai/rankings)
- **Your use case:** Match model capabilities to your task
- **Testing:** Try 2-3 models and compare results

### What happens when I run out of tokens?

- You'll receive notifications at 80% and 100%
- Once quota is reached, new requests are blocked
- Upgrade your plan or wait for monthly reset
- Usage resets on your subscription renewal date

### Can I use my own API keys?

Currently, KeystoneAgentic manages model access and you pay based on token usage through your subscription. Direct API key integration is not required.

### How secure is my data?

- All models have Zero Data Retention
- Data encrypted in transit and at rest
- Organization data isolation (your data never mixes with others)
- Role-based access control
- [Read full security documentation →](../security/zero-data-retention.md)

### Can I export my conversations?

Conversation export features are planned for future release. Currently, conversations are accessible through the chat interface.

---

## Troubleshooting

### Models not responding?

**Check:**
1. Model is synced (Models → Synced Models tab)
2. Model is activated (not deactivated)
3. You haven't exceeded your token quota
4. Internet connection is stable

**Solution:** Try a different model or refresh the page

### Document upload failing?

**Common issues:**
- File exceeds 10 MB limit
- Unsupported file format
- Password-protected PDF
- Corrupted file

**Solution:** Compress file, remove password, convert format, or try a different file

### Can't invite team members?

**Check:**
- You have Admin role (Members and Viewers can't invite)
- Your plan hasn't reached user limit
- Email address is correct

**Solution:** Upgrade plan for more users or contact support

---

## Next Steps

Now that you're set up, explore these areas:

**For Power Users:**
- [Understanding LLMs](../ai-models/understanding-llms.md) - Deep dive into AI models
- [Model Management](../ai-models/model-management.md) - Activate, configure, and optimize models
- [RAG Best Practices](../knowledge-base/rag-overview.md) - Get the most from your documents

**For Team Admins:**
- [Role-Based Permissions](../organization/roles-permissions.md) - Understand access control
- [Team Management](../organization/team-members.md) - Manage your team effectively
- [Usage Analytics](../analytics/usage-tracking.md) - Monitor and optimize usage

**For All Users:**
- [Dashboard Overview](../user-guide/dashboard.md) - Navigate the interface
- [Chat Features](../user-guide/chat.md) - Master conversation tools
- [Profile Settings](../user-guide/profile.md) - Customize your experience

---

## Getting Help

**Need assistance?**

- **Documentation:** Browse the [Main Documentation](../README.md) for detailed guides
- **Support Email:** support@keystoneagentic.com
- **Feature Requests:** Share feedback through your dashboard

---

**You're ready to start! Head to the [Dashboard](/dashboard) and begin your AI journey.**

[← Back to Main Documentation](../README.md)
