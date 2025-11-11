# Chat: Conversations with AI

[← Back to Main Documentation](../README.md)

The Chat interface is where you interact with AI models, ask questions, get assistance, and leverage your organization's knowledge base through RAG.

---

## Accessing Chat

**Navigate to:** Chat (in sidebar)

**Who can access:**
- **Admins:** Full access
- **Members:** Full access
- **Viewers:** No access (404 error)

---

## Chat Interface Overview

### Main Components

**Model Selector** (Top of page)
- Dropdown showing all synced, active models
- Click to switch models
- Shows currently selected model name
- Only displays models your organization has synced

**Message Area** (Center)
- Displays conversation history
- Your messages on the right (blue background)
- AI responses on the left (gray background)
- Scrollable to view entire conversation

**Input Box** (Bottom)
- Text area for typing messages
- Auto-resizing as you type
- Supports multi-line input
- Send button or press Enter to send

---

## Starting a Conversation

### First Steps

1. **Select a model** from dropdown (top of page)
2. **Type your message** in the input box at bottom
3. **Send message** by:
   - Pressing **Enter** (sends immediately)
   - Pressing **Shift + Enter** (new line without sending)
   - Clicking **Send** button
4. **Watch response** stream in real-time

---

### Your First Message

**What to ask:**
- Questions: "What is machine learning?"
- Instructions: "Write a professional email about..."
- Analysis: "Summarize the key points of..."
- Creative: "Generate 5 marketing taglines for..."
- Code: "Write a Python function to..."

**Tips for better responses:**
- Be specific and clear
- Provide context when needed
- Break complex requests into steps
- Iterate and refine

---

## Understanding Message Display

### Your Messages (Right Side)

**Visual:**
- Aligned to the right
- Blue background
- Timestamp (if enabled)
- Edit/delete options (coming soon)

**Content:**
- Exactly as you typed it
- Preserved formatting
- Code blocks rendered if using markdown

---

### AI Responses (Left Side)

**Visual:**
- Aligned to the left
- Gray/white background
- Model name shown (which model generated it)
- Timestamp
- Copy button (coming soon)

**Content:**
- Markdown-formatted text
- **Bold**, *italic*, lists, code blocks
- Links are clickable
- Tables rendered properly

---

## Streaming Responses

### Real-Time Generation

Most models support **streaming** - responses appear word-by-word as generated.

**What you'll see:**
- Text appears progressively
- Cursor indicates generation in progress
- Can read response while it's still generating
- Stop button appears (to cancel generation)

**Benefits:**
- Immediate feedback
- Better user experience for long responses
- Can stop early if answer is sufficient

**Non-streaming models:**
- Brief pause after sending message
- Full response appears at once
- Less common with modern models

---

## Switching Models Mid-Conversation

### How to Switch

1. Click **model dropdown** (top of page)
2. Select different model
3. Continue conversation with new model
4. Previous messages remain visible

### What Happens

**Conversation history:**
- All previous messages stay in context
- New model sees entire conversation
- Maintains continuity

**Different models, different responses:**
- Each model has unique strengths
- Compare responses by asking same question to different models
- Useful for validation or getting alternative perspectives

**Visual indicator:**
- Each AI message shows which model generated it
- Easy to track which model said what

---

## Conversation Memory & Context

### How Context Works

**AI remembers within conversation:**
- All previous messages in current conversation
- Your questions and AI's responses
- Can reference earlier parts of discussion

**Example:**
```
You: "What is Python?"
AI: [Explains Python programming language]

You: "How do I install it?"
AI: [Explains installation, knowing you're asking about Python]
```

### Context Window Limits

**What it is:**
- Maximum tokens (words) AI can process at once
- Includes your messages + AI responses + system instructions

**When you exceed it:**
- Oldest messages drop from context
- AI "forgets" early conversation
- May lose thread of discussion

**Solution:**
- Start new conversation for new topics
- Summarize key points periodically
- Use models with larger context windows for long discussions

---

## Document-Enhanced Responses (RAG)

### Automatic Document Search

When you have documents uploaded, the system automatically:

1. **Analyzes your question**
2. **Searches your documents** for relevant information
3. **Retrieves matching sections**
4. **Provides them to the AI** as context
5. **AI references your documents** in the response

**No configuration needed** - happens automatically when relevant

---

### How to Know RAG is Working

**Indicators:**
- AI references specific documents by name
- Quotes or paraphrases your uploaded content
- Provides details only found in your documents
- Answers are specific to your organization

**Example:**
```
You: "What is our vacation policy?"

AI: "According to your Employee Handbook, full-time employees
receive 15 days of vacation annually, accruing at 1.25 days
per month..."
```

---

### Maximizing RAG Effectiveness

**Upload relevant documents:**
- Add documents before asking questions about them
- Ensure documents are processed (status shows "Ready")
- Use descriptive filenames

**Ask specific questions:**
- Reference document topics
- Be clear about what you need
- Use terminology from your documents

**Verify responses:**
- Check cited information against source documents
- AI shows which documents were referenced
- Cross-reference critical facts

[Learn more about RAG →](../knowledge-base/rag-overview.md)

---

## Message Input Best Practices

### Formatting Your Messages

**Plain text:**
- Type normally for simple messages
- No special formatting needed

**Multi-line messages:**
- Press **Shift + Enter** for line breaks
- Organize complex requests into bullet points
- Separate instructions clearly

**Code in messages:**
- Wrap in backticks for inline code: `variable`
- Use triple backticks for code blocks:
```
\`\`\`python
def example():
    return "Hello"
\`\`\`
```

---

### Effective Prompt Writing

**Be specific:**
```
❌ Vague: "Tell me about marketing"
✅ Specific: "List 5 digital marketing strategies for B2B SaaS companies"
```

**Provide context:**
```
❌ No context: "Write an email"
✅ With context: "Write a professional email to a client explaining
a 2-week delay, maintaining positive tone, offering solution"
```

**Break down complex tasks:**
```
❌ "Do everything for my project"
✅ "Step 1: Outline the project structure
     Step 2: Create a timeline
     Step 3: Identify risks"
```

**Use examples:**
```
"Generate product descriptions like this example:
[paste example]

Now generate one for [your product]"
```

[Learn more about effective prompting →](../ai-models/understanding-llms.md#writing-effective-prompts)

---

## Managing Conversations

### Starting a New Conversation

**Current approach:**
- Refresh the page
- Select model and start fresh
- Previous conversation is saved (coming soon: conversation history)

**When to start new:**
- Changing topics completely
- Context window is full
- Want clean slate
- Previous conversation no longer relevant

---

### Conversation History (Coming Soon)

Planned features:
- View list of past conversations
- Resume previous conversations
- Search conversation history
- Delete old conversations
- Export conversations

---

## Model Selection Strategy

### Choosing the Right Model

**For quick questions:**
- Fast, economical models
- 8-16K context window
- Good enough for most tasks

**For complex analysis:**
- Reasoning/thinking models
- Better at logic and problem-solving
- Slower and more expensive

**For long conversations:**
- Large context window (128K+)
- Won't forget early messages
- Can process entire documents

**For document analysis:**
- Large context window
- Good at summarization
- RAG-compatible

[Learn more about choosing models →](../ai-models/understanding-llms.md#choosing-the-right-model)

---

### Comparing Models

**Try the same question with different models:**

1. Ask question with Model A
2. Switch to Model B using dropdown
3. Ask same question
4. Compare responses
5. Note which model performs better for this type of task

**Useful for:**
- Finding best model for specific tasks
- Validating important answers
- Exploring different perspectives
- Quality comparison

---

## Troubleshooting

### No Models in Dropdown

**Problem:** Dropdown is empty or says "No models available"

**Causes:**
- No models synced to organization
- All synced models are deactivated
- Permission issue

**Solutions:**
1. Go to Models → Discover
2. Sync at least one model
3. Ensure model is activated (Models → Synced Models)
4. Verify you're an Admin or Member (Viewers can't access chat)

---

### Model Not Responding

**Problem:** Message sent but no response appears

**Checks:**
1. **Internet connection** - verify you're online
2. **Model status** - check if model is currently down
3. **Token quota** - ensure you haven't exceeded limits
4. **Message length** - very long messages may time out

**Solutions:**
- Try a different model
- Refresh the page
- Shorten your message
- Check Dashboard for quota status
- Wait a minute and retry

---

### Response Stopped Mid-Generation

**Problem:** Streaming response stops abruptly

**Possible causes:**
- **Max tokens reached** - model hit output limit
- **Network interruption** - connection dropped
- **Model timeout** - response took too long

**Solutions:**
- Ask AI to continue: "Please continue your response"
- Rephrase question to be more specific
- Try a different model
- Check internet stability

---

### AI Doesn't Have Information I Uploaded

**Problem:** AI says it doesn't know something that's in your documents

**Troubleshooting:**
1. **Verify document status** - Go to Knowledge Base, ensure "Ready" status
2. **Check question relevance** - Is your question clearly related to document content?
3. **Rephrase question** - Use terminology from your documents
4. **Wait for processing** - Recently uploaded documents need time to process

**Solutions:**
- Explicitly mention the document: "According to [Document Name], what is..."
- Ask more specific questions
- Ensure document uploaded successfully
- Check document content is text-searchable

---

### Response is Incorrect or Hallucinating

**Problem:** AI provides false or made-up information

**Understanding:**
- AI models can generate plausible-sounding but incorrect info
- More common when AI lacks knowledge on topic
- Reduced by RAG but not eliminated

**Solutions:**
- **Verify facts** independently
- **Upload documents** on the topic for grounding
- **Ask for sources** - "Where does this information come from?"
- **Try different models** - some are more accurate
- **Rephrase question** to be more specific

---

## Best Practices

### For Better Responses

**DO:**
- Start with clear, specific questions
- Provide relevant context
- Use complete sentences
- Reference your documents when asking about them
- Iterate - refine based on responses

**DON'T:**
- Assume AI knows your specific situation
- Ask vague, open-ended questions without context
- Expect perfect accuracy on all topics
- Skip verification of critical information
- Use AI for real-time data (use current info sources instead)

---

### For Efficient Usage

**DO:**
- Choose appropriate model for task (don't use expensive reasoning models for simple tasks)
- Use RAG instead of pasting entire documents in chat
- Start new conversations for new topics
- Take advantage of streaming to read while generating

**DON'T:**
- Keep one conversation going indefinitely
- Paste massive amounts of text if documents can be uploaded
- Use expensive models for simple questions
- Repeatedly ask same question (refine instead)

---

### For Security & Privacy

**DO:**
- Remember all models have Zero Data Retention
- Log out on shared computers
- Be mindful of sensitive information in conversations
- Know that Admins can view all conversations

**DON'T:**
- Share passwords or API keys in chat
- Include personally identifiable information (PII) unnecessarily
- Discuss confidential strategies if you don't want Admins to see
- Assume conversations are completely private (team visibility)

---

## Chat Features Comparison

| Feature | Current Status | Coming Soon |
|---------|---------------|-------------|
| Real-time streaming | ✅ Available | - |
| Model switching | ✅ Available | - |
| RAG (document search) | ✅ Available | Enhanced relevance |
| Message history | ✅ Current session | Persistent across sessions |
| Conversation list | ❌ Not available | ✅ Planned |
| Export conversations | ❌ Not available | ✅ Planned |
| Edit messages | ❌ Not available | ✅ Planned |
| Delete messages | ❌ Not available | ✅ Planned |
| Share conversations | ❌ Not available | ✅ Planned |
| Voice input | ❌ Not available | Under consideration |
| Image upload | ❌ Not available | ✅ Planned (vision models) |

---

## Related Documentation

- **[Understanding LLMs](../ai-models/understanding-llms.md)** - Learn about tokens, context windows, and model capabilities
- **[Model Discovery](../ai-models/model-discovery.md)** - Find and sync the right models
- **[RAG Overview](../knowledge-base/rag-overview.md)** - Enhance responses with your documents
- **[Document Management](../knowledge-base/document-management.md)** - Upload and organize knowledge base

---

## Need Help?

**Model not working?**
Try a different model or check Models page for status

**RAG not finding documents?**
Verify documents are uploaded and status shows "Ready"

**General questions?**
Email support@keystoneagentic.com

---

**Chat with confidence. Get accurate, document-grounded responses.**

[← Back to Main Documentation](../README.md)
