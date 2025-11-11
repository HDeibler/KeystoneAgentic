# Zero Data Retention (ZDR)

[← Back to Main Documentation](../README.md)

KeystoneAgentic is committed to your data privacy. All AI models available through our platform come from providers with **Zero Data Retention (ZDR)** policies, ensuring your conversations and data are never stored, logged, or used for training by AI providers.

---

## What is Zero Data Retention?

**Zero Data Retention (ZDR)** means that an AI provider will **not store your data for any period of time** after processing your request.

When you send a message to an AI model with ZDR:
1. Your prompt is sent to the provider
2. The provider processes your request and generates a response
3. **Your prompt and response are immediately discarded**
4. No logs, no storage, no retention—your data never persists on the provider's systems

### Why This Matters

Without ZDR, AI providers may:
- Store your prompts and conversations indefinitely
- Use your data to train future AI models
- Retain data for analysis, research, or compliance purposes
- Keep logs that could be accessed by third parties or legal requests

**With ZDR, none of this happens.** Your data is processed and immediately forgotten.

---

## KeystoneAgentic's ZDR Commitment

### Every Model is ZDR-Compliant

KeystoneAgentic **exclusively provides access to AI models from providers with Zero Data Retention policies**. This is not optional—it's a fundamental requirement.

**What this means for you**:
- Every model you see in the Model Discovery catalog has ZDR
- Every conversation you have is never retained by the AI provider
- Every document you process is immediately discarded after use
- No exceptions, no compromises

### How We Ensure ZDR Compliance

KeystoneAgentic verifies that all accessible models have ZDR policies by:
1. **Verifying provider data policies** - Working with providers to confirm retention policies
2. **Tracking policies per model** - Monitoring each specific model endpoint
3. **Continuous updates** - Maintaining real-time policy information as providers change terms
4. **Conservative stance** - If a policy is unclear, the model is excluded from KeystoneAgentic

Only models with confirmed Zero Data Retention policies appear in your catalog.

---

## What ZDR Protects

### Your Prompts
Every message you send to an AI model is protected:
- Questions and instructions
- Context you provide
- Follow-up messages in conversations
- System prompts and configurations

**None of this is retained by the AI provider.**

### Your Documents
When you use RAG (Retrieval-Augmented Generation) with uploaded documents:
- Document chunks sent to the AI are not retained
- The AI provider never stores your document content
- After generating a response, your document data is discarded

**Your knowledge base remains private to your organization.**

### Your Conversations
Multi-turn conversations are protected:
- Previous messages in the conversation are sent as context
- The AI provider processes the full history but doesn't store it
- Each request is stateless from the provider's perspective

**Your conversation history exists only in KeystoneAgentic's secure database, not with AI providers.**

---

## ZDR vs. Training Policies

### They're Related But Different

**Zero Data Retention (ZDR)**:
- Data is **not stored** after processing
- Immediate deletion of prompts and responses
- No logs, no retention period

**No Training Policy**:
- Data is **not used to train** future AI models
- Provider may still retain data for other purposes (abuse detection, legal compliance, analytics)
- Data might be stored but not used for model improvement

### Why KeystoneAgentic Requires Both

Some providers have "no training" policies but **still retain your data**. This means:
- Your prompts are stored in logs
- Your data could be accessed by the provider
- Legal requests could expose your information
- Data breaches could compromise your privacy

**KeystoneAgentic only uses models with ZDR**, which is stricter than "no training." ZDR means:
- No retention = No training (can't train on data you don't have)
- No storage = No risk of data breaches
- No logs = No legal exposure

---

## Technical Details

### In-Memory Caching vs. Data Retention

Some AI models use **in-memory caching** for performance optimization:
- Repeated parts of prompts are temporarily cached in RAM
- This reduces processing time and costs
- Cached data is never written to disk
- Cache is cleared regularly (usually within minutes)

**KeystoneAgentic's stance**: In-memory caching is **not considered data retention** because:
- Data exists only in volatile memory
- No persistent storage occurs
- Cache is automatically cleared
- Data cannot be retrieved after processing

**Models with in-memory caching are ZDR-compliant and available through KeystoneAgentic.**

### ZDR Enforcement

KeystoneAgentic enforces ZDR at multiple levels:

**Account-Level Enforcement**:
- Your organization is configured to only access ZDR models
- This setting cannot be disabled by users
- Applies to all requests organization-wide

**Model Catalog Filtering**:
- Non-ZDR models are excluded from the Model Discovery page
- You cannot sync models without ZDR policies
- The catalog is automatically updated when policies change

**Request-Level Validation**:
- Every API request validates ZDR compliance
- Requests to non-ZDR endpoints are rejected
- No accidental data retention is possible

---

## What Happens to Your Data

### At KeystoneAgentic (Us)

We store the following **in our secure database**:
- **Your conversations**: Complete message history for your organization
- **Your documents**: Uploaded files and processed chunks for RAG
- **Your usage**: Token consumption, request counts, analytics
- **Your account data**: Names, emails, roles, organization settings

**Security measures**:
- Encrypted at rest and in transit
- Role-based access control (RBAC)
- Organization isolation (your data never mixes with others)
- Regular backups and disaster recovery
- No third-party access without your explicit consent

**We do NOT**:
- Use your data to train AI models
- Share your data with third parties
- Sell your data
- Use your conversations for marketing or analytics outside your organization

### At AI Providers (External)

When you send a request to an AI model:
1. **Request sent**: Your prompt travels through our gateway to the provider
2. **Processing**: The provider's model generates a response
3. **Response returned**: The answer comes back to you through our gateway
4. **Data discarded**: The provider immediately deletes your prompt and their response

**AI providers do NOT store**:
- Your prompts
- AI-generated responses
- Your document content
- Conversation history
- Any metadata about your requests

---

## Compliance and Legal

### GDPR Compliance

Zero Data Retention aligns with GDPR's data minimization principle:
- **Article 5(1)(c)**: Data must be adequate, relevant, and limited to what is necessary
- **Article 5(1)(e)**: Data must be kept no longer than necessary

By using ZDR models, you ensure:
- AI providers don't create additional data processing records
- No need to track provider retention periods
- Simplified compliance with data subject access requests (DSARs)
- Reduced risk of data breaches involving AI-processed content

### CCPA Compliance

California Consumer Privacy Act compliance is simplified:
- ZDR providers don't "sell" data (they don't retain it)
- No need to track downstream data sharing with AI providers
- Consumer data is processed and immediately discarded

### HIPAA and Sensitive Data

If you're processing healthcare or sensitive information:
- ZDR significantly reduces risk
- No provider-side storage means no PHI/PII retention
- Conversations with AI don't create HIPAA-covered records at the provider

**Note**: KeystoneAgentic itself stores your conversations. Ensure your own data handling complies with HIPAA and other regulations.

---

## Verification and Transparency

### How to Verify ZDR Status

**In the Model Discovery Page**:
- All models shown are pre-filtered for ZDR compliance
- Model cards display provider information
- You can research each provider's public data policy

**Provider Documentation**:
- Each AI provider publishes their data retention and privacy policies
- You can independently review provider policies for additional assurance
- KeystoneAgentic verifies these policies before making models available

### Trust but Verify

While we enforce ZDR and trust our providers:
- **Never send highly sensitive data** unless you've independently verified provider policies
- **Review provider terms** for any model you use extensively
- **Assume some risk** exists in any third-party processing
- **Use encryption** for sensitive data when possible

---

## Limitations of ZDR

### What ZDR Doesn't Protect Against

**Network Transmission**:
- Your data travels over the internet to reach AI providers
- Use HTTPS/TLS encryption (which we do) to protect data in transit
- Network intermediaries (ISPs, etc.) could theoretically intercept traffic

**KeystoneAgentic Retention**:
- We store your conversations and documents in our database
- ZDR applies to AI providers, not to KeystoneAgentic itself
- You control your data within our platform; delete conversations/documents anytime

**Your Own Device**:
- Conversations are displayed in your browser
- Browser history, cache, and local storage may contain conversation data
- Use private browsing or clear history if needed

**Accidental Exposure**:
- If you share a conversation link or screenshot, that data is exposed
- ZDR doesn't prevent you from sharing data yourself

### When ZDR Isn't Enough

For extremely sensitive use cases, consider:
- **On-premises AI**: Self-hosted models that never leave your infrastructure
- **Dedicated deployments**: Private AI instances with contractual guarantees
- **Homomorphic encryption**: Process encrypted data without decryption (cutting-edge, limited availability)

KeystoneAgentic is excellent for most business and personal use cases, but ultra-sensitive applications may require additional controls beyond ZDR.

---

## Frequently Asked Questions

### Does ZDR mean AI providers can't improve their models?

AI providers improve models using:
- Publicly available datasets
- Licensed training data
- Synthetic data generation
- Research and development separate from user prompts

**ZDR only means they don't use your specific prompts for training.** They still improve their models through other methods.

---

### Can AI providers see my data even if they don't retain it?

Yes, briefly. Providers must process your data to generate responses. ZDR means they delete it immediately after, but humans or systems at the provider could theoretically observe data during processing.

**For maximum privacy**: Don't send data you wouldn't want anyone to see, even momentarily.

---

### What if a provider's ZDR policy changes?

KeystoneAgentic monitors provider policies continuously. If a provider changes from ZDR to data retention:
1. The model's policy status is updated
2. KeystoneAgentic removes the model from your available catalog
3. You'll be notified if a synced model is no longer ZDR-compliant
4. You'll need to select an alternative model

---

### Does ZDR affect AI response quality?

No. ZDR is about what happens **after** processing, not during. The AI generates responses the same way whether or not it retains data afterward.

---

### Can I use non-ZDR models if I want to?

No. KeystoneAgentic enforces ZDR organization-wide as a core privacy commitment. If you need non-ZDR models, you would need to use a different platform.

---

### Does ZDR cost more?

Not necessarily. Many providers offer ZDR at the same price as data-retaining endpoints. KeystoneAgentic's pricing is based on token usage, not ZDR compliance.

---

## Comparison: ZDR vs. Traditional AI Platforms

| Aspect | KeystoneAgentic (ZDR) | Traditional AI Platforms |
|--------|----------------------|--------------------------|
| **Data Retention** | Zero—immediately discarded | Often retained for 30+ days |
| **Training on Your Data** | Never | Sometimes (opt-out required) |
| **Provider Logs** | No logs created | Logs for analytics, abuse detection |
| **GDPR Compliance** | Simplified (no provider retention) | Complex (must track provider retention) |
| **Data Breach Risk** | Lower (no provider-side storage) | Higher (stored data can be breached) |
| **Legal Requests** | Nothing to provide (no retention) | Stored data can be subpoenaed |
| **Model Selection** | Only ZDR models | All models, including non-ZDR |
| **User Control** | Automatic ZDR enforcement | Must manually enable privacy settings |

---

## Best Practices for Privacy

### Even with ZDR, follow these guidelines:

**Minimize Sensitive Data**:
- Don't send passwords, API keys, or secrets to AI
- Redact personal information when possible
- Use synthetic or anonymized data for testing

**Delete When Done**:
- Remove conversations you no longer need
- Delete uploaded documents after projects complete
- Manage your own KeystoneAgentic data retention

**Use Strong Access Controls**:
- Limit team member roles appropriately (Admin, Member, Viewer)
- Review team access quarterly
- Remove former employees immediately

**Educate Your Team**:
- Ensure users understand ZDR and its limitations
- Train on what data is safe to send to AI
- Create organizational policies for AI usage

**Monitor Usage**:
- Review analytics to understand what data flows through AI
- Audit conversations periodically for compliance
- Track which models are used most

---

## Additional Resources

### Understanding Zero Data Retention
Learn more about how ZDR policies are verified and maintained:
[OpenRouter ZDR Documentation](https://openrouter.ai/docs/features/zdr)

### Provider-Specific Policies
Research individual AI providers' data retention policies through their official websites and privacy documentation.

---

## Contact and Support

### Questions about ZDR?
- **Email**: privacy@keystoneagentic.com
- **Support**: support@keystoneagentic.com

### Report a Policy Violation
If you believe a model is not honoring its ZDR commitment:
- Email: privacy@keystoneagentic.com
- Include: Model name, timestamp, and details
- We will investigate immediately

---

**Your privacy is non-negotiable. With Zero Data Retention, your conversations stay yours—and yours alone.**

[← Back to Main Documentation](../README.md)
