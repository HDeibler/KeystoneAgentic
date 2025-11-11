# First Steps After Sign Up

Congratulations on creating your KeystoneAgentic account! This guide will walk you through the essential setup steps to get the most out of the platform.

---

## 1. Explore Your Dashboard

After logging in, you'll land on your **Dashboard**. This is your command center for AI operations.

### What You'll See

**Quick Actions**
- **New Chat**: Start a conversation with an AI model (coming soon)
- **Browse Models**: Explore available AI models
- **Upload Documents**: Add files to your knowledge base
- **View Analytics**: See usage statistics (Admin only)

**Organization Status**
- Current plan (Trial, Starter, Professional, or Enterprise)
- Days remaining in trial (if applicable)
- Subscription status

**Statistics**
- **User Seats**: How many team members you can add
- **Monthly Tokens**: Your token quota and current usage
- **Requests**: Total API requests this month
- **Conversations**: Active chat sessions

**Recent Activity**
- Recent conversations (when available)
- Recently synced models

---

## 2. Sync Your First AI Models

Before you can chat with AI, you need to add models to your organization.

### Browse Available Models

1. Click **Browse Models** from the dashboard or navigate to **Models** in the sidebar
2. You'll see the **Model Discovery** tab with hundreds of available models

### Understanding Model Information

Each model card shows:
- **Model Name**: The official identifier
- **Provider**: Who created the model (OpenAI, Anthropic, Google, etc.)
- **Description**: What the model is good at
- **Context Window**: Maximum tokens it can process (e.g., 128K = ~96,000 words)
- **Pricing**: Cost per 1 million input/output tokens
- **Features**: Badges for capabilities (Streaming, Vision, Reasoning, etc.)
- **Uptime**: Reliability in the last 30 minutes

### Filter Models

Use filters to find the right model:
- **Search**: Type model name, provider, or keywords
- **Provider**: Filter by OpenAI, Anthropic, Google, etc.
- **Context Window**: Set minimum/maximum token limits
- **Capabilities**: Filter by features (Vision, Function Calling, Reasoning)
- **Price**: Set maximum price per 1M tokens
- **Uptime**: Show only highly reliable models

### Sync a Model

1. Find a model you want to use
2. Click the **Sync** button on its card
3. The model is added to your organization instantly
4. A success message confirms the sync

**Recommended Starter Models:**
- **GPT-4o**: Fast, versatile, good for most tasks
- **Claude 3.5 Sonnet**: Excellent reasoning and writing
- **GPT-4o Mini**: Very affordable for high-volume use
- **Claude 3 Opus**: Best for complex tasks requiring deep thought

### View Synced Models

1. Click the **Synced Models** tab
2. See all models you've added to your organization
3. Activate/deactivate models as needed
4. Set a default model for your organization

---

## 3. Invite Your Team

If you're collaborating with others, invite them to your organization.

### How to Invite Members

1. Navigate to **Organization** → **Team Members** in the sidebar
2. Click **Invite Member**
3. Enter their information:
   - **Name**: Their full name
   - **Email**: Their work email (they'll use this to log in)
   - **Role**: Select Admin, Member, or Viewer ([learn about roles](/docs/organization/roles-permissions))
4. Click **Send Invite**

### What Happens Next

- The new member receives an email invitation
- They click the link to set their password
- They log in and join your organization
- They appear in your team members list

### Choosing the Right Role

- **Admin**: Full control (billing, settings, team management) - Use sparingly
- **Member**: Can use AI features, manage models and knowledge - Most team members
- **Viewer**: Read-only access to view data - For stakeholders

**Tip**: Start with fewer Admins. You can always promote Members later.

---

## 4. Upload Your First Document

Build a knowledge base so AI can reference your specific information.

### Uploading Documents

1. Navigate to **Knowledge Base** → **Documents**
2. Click **Upload Document**
3. Select a file from your computer:
   - Supported formats: PDF, DOCX, TXT, MD, and more
   - Maximum file size: 10 MB per file
4. Click **Upload**

### What Happens to Your Document

1. **Upload**: File is securely stored
2. **Processing**: Text is extracted from the file
3. **Chunking**: Content is split into searchable segments
4. **Embedding**: AI creates vector representations for semantic search
5. **Ready**: Document is available for RAG in conversations

### Using Documents in Conversations (Coming Soon)

Once uploaded, documents automatically enhance AI responses:
- Ask questions about your documents
- AI finds relevant sections
- Responses are grounded in your actual data
- No hallucinations—answers cite your sources

---

## 5. Set Up Billing (Before Trial Ends)

If you're on a trial, add a payment method before it expires to avoid service interruption.

### Add a Payment Method

1. Navigate to **Organization** → **Billing**
2. Click **Add Payment Method**
3. Enter your credit card information (Stripe secure checkout)
4. Select your desired plan:
   - **Starter**: $29/month, 500K tokens, 5 users
   - **Professional**: $99/month, 2M tokens, 20 users
   - **Enterprise**: $499/month, 10M tokens, unlimited users
5. Click **Subscribe**

### Trial to Paid Transition

- Your trial continues until the 14-day period ends
- On day 15, your subscription begins
- You're charged on your subscription anniversary each month
- Usage quotas reset monthly

### Payment & Invoicing

- Payments are processed via Stripe
- Invoices are emailed automatically
- View payment history in **Billing** settings
- Update or change your payment method anytime

---

## 6. Monitor Your Usage

Stay aware of your token consumption to avoid unexpected quota limits.

### Check Your Quota

**Dashboard Overview**
- See current usage vs. monthly allocation
- Track requests and conversations
- View user seat utilization

**Detailed Analytics** (Admin only)
1. Navigate to **Analytics**
2. View detailed breakdowns:
   - Tokens used per user
   - Tokens used per model
   - Conversations and messages
   - Document uploads

### Quota Warnings

- **80% Usage**: Warning notification appears
- **100% Usage**: Hard limit—new requests are blocked
- **110% Grace Period**: Temporary buffer before strict enforcement

### What to Do When Quota is Low

- **Upgrade Plan**: Increase your monthly token allocation
- **Wait for Reset**: Quotas reset on your subscription anniversary
- **Optimize Usage**: Use cheaper models for simpler tasks

---

## 7. Customize Your Profile

Make your account yours by updating your profile.

### Edit Your Profile

1. Click your name in the top-right corner
2. Select **Profile**
3. Update:
   - **Name**: Your display name
   - **Email**: Your login email (requires verification if changed)
   - **Password**: Click **Change Password** to update via email

### Profile Picture (Coming Soon)

Custom avatars will be available in a future update.

---

## 8. Explore Advanced Features

Once you're comfortable with the basics, explore these features:

### API Keys (Coming Soon)
Generate keys for programmatic access to KeystoneAgentic from your applications.

### MCP Integration (Advanced)
Connect custom tools and data sources via Model Context Protocol.

### Analytics & Reporting
Deep dive into usage patterns, user behavior, and model performance.

---

## Quick Reference Checklist

Use this checklist to ensure you've completed essential setup:

- [ ] Explored the dashboard
- [ ] Synced at least 2-3 AI models
- [ ] Set a default model
- [ ] Invited team members (if applicable)
- [ ] Uploaded a test document
- [ ] Reviewed billing and plan options
- [ ] Updated your profile
- [ ] Checked organization settings
- [ ] Reviewed user roles and permissions
- [ ] Bookmarked the documentation

---

## Next Steps

You're all set! Here's what to learn next:

- **[Understanding AI Models](/docs/ai-models/understanding-llms)** - Learn about tokens, context windows, and reasoning models
- **[User Roles & Permissions](/docs/organization/roles-permissions)** - Understand what each role can do
- **[Knowledge Base Guide](/docs/knowledge-base/rag-overview)** - Make the most of RAG
- **[Dashboard Guide](/docs/user-guide/dashboard)** - Navigate the interface like a pro

---

## Need Help?

- **Email**: support@keystoneagentic.com
- **Documentation**: [Full User Guide](/docs/user-guide/dashboard)
- **Status**: status.keystoneagentic.com

Happy building! 🚀
