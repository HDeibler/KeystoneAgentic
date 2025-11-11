# User Roles & Permissions

[← Back to Main Documentation](../README.md)

KeystoneAgentic uses role-based access control (RBAC) to manage team member access. This guide explains the three roles and their exact permissions.

---

## The Three Roles

### Admin - Full Organization Control

**Access Level:** Complete control over organization, billing, settings, and team management

**Best For:**
- Organization owners
- Technical leaders
- Billing managers
- Team administrators

**Recommended Count:** 2-3 Admins per organization for redundancy

---

### Member - Full Product Access

**Access Level:** Use all AI features, manage models and documents, but no billing or organization settings access

**Best For:**
- Developers and engineers
- Content creators
- Data analysts
- Most team members

**Recommended Count:** As many as needed (within plan limits)

---

### Viewer - Read-Only Access

**Access Level:** View organization data without making changes

**Best For:**
- Stakeholders and executives
- Auditors
- Temporary contractors
- External consultants
- Interns

**Recommended Count:** As needed for reporting and oversight

---

## Complete Permission Matrix

**Quick Reference:** What each role can do

| Permission Category | Admin | Member | Viewer |
|:-------------------|:-----:|:------:|:------:|
| **Profile Management** |
| View own profile | ✅ | ✅ | ✅ |
| Edit own profile | ✅ | ✅ | ✅ |
| Edit other profiles | ✅ | ❌ | ❌ |
| **Team Management** |
| View team members | ✅ | ✅ | ❌ |
| Invite team members | ✅ | ❌ | ❌ |
| Edit team members | ✅ | ❌ | ❌ |
| Change member roles | ✅ | ❌ | ❌ |
| Remove team members | ✅ | ❌ | ❌ |
| Suspend/reactivate users | ✅ | ❌ | ❌ |
| **AI Models** |
| View model catalog | ✅ | ✅ | ❌ |
| Sync new models | ✅ | ✅ | ❌ |
| Manage synced models | ✅ | ✅ | ❌ |
| **Knowledge Base** |
| View documents | ✅ | ✅ | ❌ |
| Upload documents | ✅ | ✅ | ❌ |
| Delete documents | ✅ | ✅ | ❌ |
| **Conversations** |
| Start conversations | ✅ | ✅ | ❌ |
| View own conversations | ✅ | ✅ | ❌ |
| View all conversations | ✅ | ❌ | ❌ |
| **Organization Settings** |
| View org settings | ✅ | ❌ | ❌ |
| Edit org settings | ✅ | ❌ | ❌ |
| **Billing** |
| View billing | ✅ | ❌ | ❌ |
| Manage billing | ✅ | ❌ | ❌ |
| **API Keys** |
| Manage API keys | ✅ | ❌ | ❌ |

---

## Detailed Permissions by Category

### Profile & Account

**All Roles Can:**
- View their own profile information
- Edit their own name and email
- Change their own password
- View their assigned role
- Log out of the platform

**Only Admins Can:**
- View other users' profiles
- Edit other users' information
- View complete team directory

**Viewers Cannot:**
- View team member list at all
- See other users' profiles

---

### Team Management

**Admins Have Full Control:**

*Viewing:*
- See complete team member list
- View member names, emails, roles
- See member status (active, invited, suspended, deleted)
- Filter and search team members
- View deactivated members

*Inviting:*
- Send email invitations
- Assign roles to new members
- Set initial permissions

*Managing:*
- Edit any member's profile
- Change member roles (promote/demote)
- Remove members from organization
- Suspend user accounts
- Reactivate suspended or deleted users
- Resend invitation emails

**Members Can:**
- View team member list
- See names, emails, and roles
- Identify who they're working with
- Cannot make any changes

**Viewers Cannot:**
- View team members page at all
- See who else is in the organization

---

### AI Model Management

**Admins & Members Can:**

*Model Discovery:*
- Browse full model catalog (200+ models)
- Search and filter models
- View model specs (context window, pricing, capabilities)
- Read model descriptions
- Check real-time uptime

*Model Syncing:*
- Sync new models to organization
- Add models from any provider
- Sync multiple models

*Model Management:*
- View all synced models
- Activate and deactivate models
- Set default organization model
- Delete synced models
- Configure model settings

**Viewers Cannot:**
- Access Models page at all
- View model catalog
- See synced models
- Use any model features

---

### Knowledge Base & Documents

**Admins & Members Can:**

*Uploading:*
- Upload documents (PDF, DOCX, TXT, MD, RTF, CSV)
- Multiple file uploads
- Monitor processing status

*Managing:*
- View all uploaded documents
- See document metadata
- Check processing status
- View chunk counts
- Delete documents
- Organize knowledge base

*Using:*
- Documents automatically available for RAG
- Reference documents in conversations

**Viewers Cannot:**
- Access Knowledge Base section
- View uploaded documents
- Upload new documents
- Delete documents

---

### Conversations & Chat

**Admins Can:**
- Start new AI conversations
- Use all synced models
- Switch models mid-conversation
- View their own conversation history
- View ALL organization conversations (including others')
- Delete any conversation

**Members Can:**
- Start new AI conversations
- Use all synced models
- Switch models mid-conversation
- View their own conversation history
- Cannot view other members' conversations
- Delete only their own conversations

**Viewers Cannot:**
- Access Chat page
- Start conversations
- Send messages
- View any conversations

---

### Organization Settings

**Admins Can:**
- View organization name and slug
- Edit organization name
- View organization status (trial, active, etc.)
- View quotas and limits
- Configure organization-wide settings
- View usage statistics
- Access organization-level controls

**Members & Viewers Cannot:**
- Access Organization Settings
- View organization configuration
- See organizational details beyond basic info
- Modify any organization settings

---

### Billing & Subscriptions

**Admins Can:**
- View current subscription plan
- See plan limits (tokens, users, storage)
- Access billing dashboard
- View payment methods
- Update credit card information
- Change subscription (upgrade/downgrade)
- View invoice history
- Download invoices
- Manage subscription status
- Cancel or reactivate subscription

**Members Can:**
- View current plan name on Dashboard
- See basic plan limits (token quota)

**Viewers Cannot:**
- View plan information
- Access billing in any way

---

### API Keys

**Admins Can:**
- View all organization API keys (prefixes only)
- Create new API keys
- Name and configure keys
- See key creation dates
- View last-used timestamps
- Revoke (delete) API keys
- Manage key permissions

**Members & Viewers Cannot:**
- View API keys
- Create API keys
- Access API keys section at all

**Important:** API keys inherit the creator's permissions. Admin-created keys have Admin-level access.

---

## Changing User Roles

### How to Change Roles (Admins Only)

**Navigate to:** Settings → Organization → Members

1. Find the user in the team list
2. Click the **role dropdown** next to their name
3. Select new role: Admin, Member, or Viewer
4. Confirm the change
5. Changes take effect **immediately**

### Immediate Effect

When you change someone's role:
- ✅ New permissions apply instantly
- ✅ Restricted pages become inaccessible (404)
- ✅ New capabilities appear
- ❌ No logout required
- ❌ No page refresh needed

**User Experience:**
- If they're on a page they can no longer access, they'll get a "Page Not Found" error
- New buttons and features appear based on new role
- Previous capabilities may disappear

---

## Permission Boundaries

### What Happens When Access is Denied?

**Restricted Pages:**
```
User navigates to /settings/billing (Viewer role)
→ Sees "404 Not Found"
→ Redirected to Dashboard
→ Page existence not revealed
```

**Restricted Actions:**
```
Member clicks "Manage Billing" (if visible)
→ Shows error: "Insufficient permissions"
→ No action performed
→ Prompted to contact Admin
```

### UI Behavior

**Hidden Elements:**
- Features you'll never need in your role disappear
- Example: Members never see "Manage Billing" button

**Disabled Elements:**
- Features you might need later but can't use now are shown but disabled
- Example: "Sync" button disabled when model already synced

**Visible but Restricted:**
- Some elements visible to show what's possible, but clicking triggers permission error
- Example: Upgrade plan banner for Members (action requires Admin)

---

## Role Change Scenarios

### When to Promote Member → Admin

**Good Reasons:**
- ✅ Need to manage billing/subscription
- ✅ Responsible for team management
- ✅ Managing organization strategy
- ✅ Promoted to managerial role
- ✅ Backup Admin needed

**Poor Reasons:**
- ❌ "Just to try something"
- ❌ One-time billing update (Admin can do it for them)
- ❌ Temporary need (ask Admin to help instead)

### When to Demote Admin → Member

**Good Reasons:**
- ✅ No longer managing team
- ✅ Role change in organization
- ✅ Reducing Admin count for security
- ✅ Moving to individual contributor role

### When to Use Viewer Role

**Perfect For:**
- ✅ Executives wanting reports
- ✅ Stakeholders needing visibility
- ✅ Auditors reviewing usage
- ✅ Consultants observing
- ✅ Interns with limited access

**Not For:**
- ❌ Active contributors
- ❌ People who need to "do things"
- ❌ Testing or experimentation

---

## Special Cases & FAQs

### What if all Admins leave the organization?

**Problem:** Organization becomes locked - nobody can manage billing, team, or settings

**Solution:** Contact support@keystoneagentic.com immediately

**Prevention:** Always maintain **at least 2 Admins**

---

### Can users have different roles in different organizations?

**Yes!** Roles are organization-specific.

**Example:**
- You're an Admin in "Company A"
- You're a Member in "Company B"
- You're a Viewer in "Company C"

Switch organizations using the dropdown in top navigation. Your permissions change automatically.

---

### Can Admins see everyone's conversations?

**Yes.** Admins have full visibility into all organization conversations for:
- Analytics and reporting
- Compliance and auditing
- Support and troubleshooting
- Usage monitoring

**Privacy Note:** Use responsibly. Access others' conversations only when necessary for legitimate organizational purposes.

---

### Can one person belong to multiple organizations?

**Yes!** One email address can join multiple organizations.

Use the organization switcher (click org name in navigation) to move between them. Each organization has independent:
- Roles and permissions
- Billing and subscriptions
- Models and documents
- Conversations and history

---

### What counts toward user limits?

**Counts toward limit:**
- Active users
- Invited users (pending acceptance)
- Suspended users

**Does NOT count:**
- Deleted users
- Left organization

**To free up seats:** Remove or delete inactive users

---

### Can Members invite other Members?

**No.** Only Admins can invite new team members.

**If you're a Member and need to add someone:**
1. Contact your organization's Admin
2. Provide the new member's email and suggested role
3. Admin sends the invitation

---

## Best Practices

### For Admins: Security & Access Management

**DO:**
- ✅ Assign minimum necessary role (least privilege principle)
- ✅ Maintain 2-3 Admins for redundancy
- ✅ Review team roles quarterly
- ✅ Remove former employees immediately
- ✅ Use Viewer role for stakeholders
- ✅ Document who has what access

**DON'T:**
- ❌ Make everyone Admin "for convenience"
- ❌ Leave inactive accounts with access
- ❌ Grant Admin for single-use access
- ❌ Ignore role change requests
- ❌ Share Admin credentials

---

### For Members: Effective Collaboration

**DO:**
- ✅ Request Admin access only when truly needed
- ✅ Ask Admins to perform one-off tasks
- ✅ Understand your role's boundaries
- ✅ Contribute through model syncing and document uploads
- ✅ Report issues to Admins

**DON'T:**
- ❌ Try to bypass permissions
- ❌ Share login credentials
- ❌ Assume you need Admin for everything
- ❌ Repeatedly request unnecessary promotions

---

### For Viewers: Maximizing Read-Only Access

**DO:**
- ✅ Use access to stay informed
- ✅ Request specific reports from Admins
- ✅ Provide feedback on observations
- ✅ Ask clarifying questions
- ✅ Respect the observation-only role

**DON'T:**
- ❌ Request promotion just to experiment
- ❌ Expect to perform actions
- ❌ Complain about limitations (it's by design)

---

## Requesting Role Changes

### If You Need More Access

1. **Identify specific need** - "I need to invite a contractor"
2. **Find your Admins** - Check Team Members list
3. **Contact Admin** - Email or message
4. **Explain requirement** - Why you need the access
5. **Suggest duration** - Temporary or permanent?

### Admins: Evaluating Requests

**Questions to Ask:**
- Is this request legitimate for their job function?
- Is it a one-time need or ongoing?
- Can I do this action for them instead?
- Does this require training or guidance?
- Is there risk in granting this access?

**Good Request:** "I'm now managing the team and need to invite/remove members"
→ Promote to Admin

**Questionable Request:** "I want to see billing just out of curiosity"
→ Deny or provide summary without full access

---

## Role Comparison Summary

<table>
<tr>
<th>Aspect</th>
<th>Admin</th>
<th>Member</th>
<th>Viewer</th>
</tr>
<tr>
<td><strong>Primary Purpose</strong></td>
<td>Manage organization</td>
<td>Use AI features</td>
<td>Observe & report</td>
</tr>
<tr>
<td><strong>Billing Access</strong></td>
<td>Full control</td>
<td>None</td>
<td>None</td>
</tr>
<tr>
<td><strong>Team Management</strong></td>
<td>Invite, edit, remove</td>
<td>View only</td>
<td>No access</td>
</tr>
<tr>
<td><strong>AI Models</strong></td>
<td>Full control</td>
<td>Full control</td>
<td>No access</td>
</tr>
<tr>
<td><strong>Knowledge Base</strong></td>
<td>Full control</td>
<td>Full control</td>
<td>No access</td>
</tr>
<tr>
<td><strong>Conversations</strong></td>
<td>All conversations</td>
<td>Own conversations</td>
<td>No access</td>
</tr>
<tr>
<td><strong>Analytics</strong></td>
<td>Full details</td>
<td>Basic dashboard</td>
<td>None</td>
</tr>
<tr>
<td><strong>Typical Count</strong></td>
<td>2-3</td>
<td>Most of team</td>
<td>As needed</td>
</tr>
</table>

---

## Next Steps

- **[Team Members Guide](team-members.md)** - Invite and manage your team
- **[Quick Start](../getting-started/quickstart.md)** - Get started with KeystoneAgentic
- **[Dashboard Overview](../user-guide/dashboard.md)** - Navigate the platform

---

## Need Help?

**Questions about permissions?**
Email: support@keystoneagentic.com

**Need a role change?**
Contact your organization's Admin

**Lost all Admin access?**
Email support immediately: support@keystoneagentic.com

---

**Clear roles enable secure, effective collaboration.**

[← Back to Main Documentation](../README.md)
