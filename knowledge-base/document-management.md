# Document Management

Build a knowledge base by uploading documents that AI can reference in conversations. This guide shows you how to upload, organize, and manage your documents.

---

## What is a Knowledge Base?

A **knowledge base** is a collection of documents that AI models can search and reference when generating responses. Instead of relying solely on training data, AI uses your specific documents to provide accurate, grounded answers.

**Benefits**:
- AI answers questions based on your actual data
- Reduces hallucinations (AI making up information)
- Keeps responses relevant to your organization
- No need to include full context in every prompt

**How it works**: See [RAG Overview](/docs/knowledge-base/rag-overview)

---

## Accessing Document Management

1. Navigate to **Knowledge Base** → **Documents** in the sidebar
2. View all uploaded documents for your organization
3. Upload, manage, and delete documents

---

## Uploading Documents

### Supported File Types

KeystoneAgentic supports common document formats:
- **PDF**: Portable Document Format
- **DOCX**: Microsoft Word documents
- **TXT**: Plain text files
- **MD**: Markdown files
- **Additional formats** (check upload dialog for full list)

### File Size Limits

- **Maximum file size**: 10 MB per file
- **No limit** on number of files
- **Organization quota**: Total storage based on plan

### How to Upload

1. Click **Upload Document** button
2. Select file from your computer (or drag and drop)
3. File uploads immediately
4. Processing begins automatically

### What Happens After Upload

1. **Upload**: File is securely stored
2. **Text Extraction**: Content is extracted from the file
3. **Chunking**: Document is split into searchable segments (chunks)
4. **Embedding Generation**: AI creates vector representations for semantic search
5. **Indexing**: Chunks are indexed for fast retrieval
6. **Ready**: Document is available for use in conversations

**Processing time**: Usually 10-60 seconds depending on file size

### Who Can Upload Documents?

- **Admins**: Yes
- **Members**: Yes
- **Viewers**: No

[See role permissions](/docs/organization/roles-permissions)

---

## Document List Overview

### What You'll See

**Document Table**:
- **Filename**: Original name of uploaded file
- **Upload Date**: When the document was added
- **File Size**: Size of the original file
- **Status**: Processing, Ready, or Error
- **Chunks**: Number of segments created
- **Actions**: Edit, Delete buttons

**Status Indicators**:
- **Processing**: Document is being chunked and embedded (yellow)
- **Ready**: Available for RAG in conversations (green)
- **Error**: Processing failed (red, with error message)

---

## Managing Documents

### Viewing Document Details

Click on a document to see:
- Full filename and path
- Upload timestamp
- File size and type
- Processing status
- Number of chunks created
- Chunk preview (text segments)

### Editing Document Metadata

1. Click **Edit** button on a document
2. Update the **document name** (optional, for organization)
3. Add **description** or **tags** (coming soon)
4. Click **Save Changes**

**Note**: Editing metadata does not reprocess the document.

### Deleting Documents

1. Find the document you want to remove
2. Click **Delete** button
3. Confirm deletion in the dialog
4. Document and all its chunks are permanently removed

**Important**:
- Deletion is permanent (cannot be undone)
- Removes document from all future conversations
- Existing conversations that used this document are unaffected (they retain context)

### Who Can Delete Documents?

- **Admins**: Yes
- **Members**: Yes
- **Viewers**: No

---

## Understanding Document Chunking

### What is Chunking?

**Chunking** splits your document into smaller, overlapping segments (chunks) for better AI retrieval.

**Why chunk documents?**
- AI context windows have token limits
- Searching smaller segments is more accurate
- Relevant sections are easier to find
- Irrelevant parts don't waste tokens

### How Chunks Work

**Example**:
- Your document: 50-page research paper
- Chunks created: 200 chunks (each ~500 tokens)
- AI search: Finds the 3 most relevant chunks
- Context sent to AI: Only those 3 chunks (~1,500 tokens)

**Result**: AI has precisely the information it needs without processing the entire 50 pages.

### Chunk Size

KeystoneAgentic uses optimized chunk sizes:
- **Default chunk size**: ~500 tokens (~375 words)
- **Overlap**: Chunks overlap by 50 tokens to preserve context
- **Dynamic sizing**: Respects paragraph and section boundaries when possible

**You don't need to configure this**—chunking happens automatically with best-practice settings.

---

## Document Processing Errors

### Common Errors

**"Failed to extract text"**:
- **Cause**: File is corrupted, password-protected, or unsupported format
- **Solution**: Verify file opens correctly, remove password protection, convert to supported format

**"File too large"**:
- **Cause**: File exceeds 10 MB limit
- **Solution**: Compress file, split into smaller documents, or remove images/media

**"Quota exceeded"**:
- **Cause**: Organization storage limit reached
- **Solution**: Delete unused documents, upgrade plan for more storage

**"Processing timeout"**:
- **Cause**: Document is extremely long or complex
- **Solution**: Split into smaller files, simplify formatting

### Retrying Failed Uploads

1. Delete the failed document
2. Fix the underlying issue (file format, size, etc.)
3. Re-upload the corrected file

---

## Searching and Filtering Documents

### Search Bar

Type to search documents by:
- Filename
- Content (searches document text)
- Upload date

### Filter by Status

- **All Documents**: Show all statuses
- **Ready**: Only documents available for use
- **Processing**: Documents currently being indexed
- **Error**: Failed uploads

### Sort Options

Click column headers to sort by:
- **Name**: Alphabetical
- **Date**: Newest or oldest first
- **Size**: Largest or smallest first
- **Chunks**: Most or fewest chunks

---

## Best Practices

### Document Preparation

**Before uploading**:
- **Remove sensitive data**: Passwords, API keys, personal info
- **Clean formatting**: Remove excessive whitespace, headers/footers
- **Convert to text-friendly formats**: PDF or DOCX preferred
- **Split large files**: Break 100+ page documents into sections

**Organize logically**:
- Use clear, descriptive filenames
- Group related documents in batches
- Maintain consistent naming conventions

### Document Maintenance

**Regular review** (quarterly):
- Delete outdated documents
- Update documents with newer versions
- Remove duplicates
- Archive unused documents

**Version control**:
- Include version/date in filename (e.g., "Policy_2024-01.pdf")
- Delete old versions when uploading new ones
- Keep changelog if documents update frequently

### Optimizing for RAG

**Write AI-friendly documents**:
- Use clear headings and sections
- Include keywords relevant to potential queries
- Avoid overly technical jargon (unless necessary)
- Structure information hierarchically

**Document granularity**:
- One topic per document is better than one massive file
- 5-50 page documents work best
- Split large manuals by chapter

---

## Document Storage and Privacy

### Where Documents are Stored

- **KeystoneAgentic database**: Securely stored in our database
- **Encrypted at rest**: All documents encrypted
- **Organization isolation**: Your documents never mix with other organizations
- **Backups**: Regular backups for disaster recovery

### Data Retention

- **While active**: Documents stored indefinitely
- **After deletion**: Permanently removed from database within 24 hours
- **Backup retention**: Deleted documents removed from backups within 30 days

### Privacy

- **Not shared**: Documents are never shared with other organizations
- **Not used for training**: Your documents are not used to train AI models
- **Access control**: Only users with appropriate roles can view/upload/delete

**AI Provider Privacy**:
- Document chunks sent to AI for processing
- Zero Data Retention: AI providers don't store your document content
- Immediate discard after response generation

[Learn more about ZDR](/docs/security/zero-data-retention)

---

## Usage Limits and Quotas

### Plan-Based Limits

- **Trial**: 100 MB total storage
- **Starter**: 1 GB total storage
- **Professional**: 10 GB total storage
- **Enterprise**: 100 GB total storage

### What Counts Toward Quota

- Original file size (not chunk size)
- All documents, regardless of status
- Deleted documents free up space immediately

### Managing Storage

**Check usage**:
- View storage usage in Organization Settings
- See per-document size in document list

**When approaching limit**:
- Delete unused documents
- Compress large files before uploading
- Upgrade plan for more storage

---

## Bulk Operations (Coming Soon)

Future features for managing multiple documents:

### Bulk Upload
- Upload multiple files at once (drag and drop folder)
- Queue processing for large batches
- Progress indicator for batch uploads

### Bulk Delete
- Select multiple documents with checkboxes
- Delete all selected at once
- Confirm before permanent deletion

### Bulk Tagging
- Assign tags to multiple documents
- Filter by tags
- Organize documents into categories

---

## Troubleshooting

### Document Stuck in "Processing"
**Cause**: Processing is taking longer than expected

**Solutions**:
- Wait 5-10 minutes (large files take time)
- Refresh the page to check status
- If stuck for 30+ minutes, delete and re-upload

---

### Can't Upload Documents
**Possible causes**:
- You're a Viewer (no upload permissions)
- File exceeds 10 MB
- Storage quota exceeded
- Unsupported file format

**Solutions**:
- Ask Admin for Member role
- Compress file or split into smaller pieces
- Delete unused documents to free space
- Convert to supported format (PDF, DOCX, TXT)

---

### Document Not Appearing in Conversations
**Possible causes**:
- Still processing (status not "Ready")
- RAG not enabled in conversation
- Document chunks don't match query

**Solutions**:
- Wait for processing to complete
- Ensure RAG is enabled (conversation settings)
- Refine your query to match document content

---

### Chunks Seem Wrong
**Issue**: Chunks are not breaking at logical places

**Explanation**:
- Chunking is automatic and optimized
- Overlapping ensures context isn't lost
- AI search finds relevant chunks regardless of boundaries

**No action needed** in most cases—the system is working as designed.

---

## Next Steps

- **[RAG Overview](/docs/knowledge-base/rag-overview)** - Understand how AI uses your documents
- **[Using RAG in Conversations (Coming Soon)** (Coming Soon) - Enable document search in chats
- **[Analytics (Coming Soon)** - Track document usage

---

**Build your knowledge base and let AI become an expert in your domain.**
