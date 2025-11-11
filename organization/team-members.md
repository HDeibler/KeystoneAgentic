# Managing Team Members

[← Back to Main Documentation](../README.md)

Collaborate effectively by inviting team members, assigning roles, and managing access. This comprehensive guide covers everything you need to know about team management in KeystoneAgentic.

---

## Accessing Team Management

**Navigate to:** Settings → Organization → Members

**Who can access:**
- **Admins:** Full access (view, invite, edit, remove, change roles)
- **Members:** View-only access (see team list, names, emails, roles)
- **Viewers:** No access (404 error if attempting to navigate)

---

## Understanding the Team Members Interface

### Main View

When you open the Team Members page, you'll see:

**Page Header**
- Title: "Team Members"
- Description: Context about managing your team
- Action buttons (Admins only):
  - **Show/Hide Deactivated** - Toggle visibility of suspended and deleted users
  - **Invite Member** - Add new team members

**Member List**
Each team member displays as a card showing:
- **Name or Email** - Display name (or email if no name set)
- **Email Address** - Login email (shown below name)
- **Role Badge** - "Admin" badge for administrators
- **Status Badges** - Invited, Suspended, or Deleted indicators
- **"You" Badge** - Your own card is highlighted in blue with "You" badge
- **Action Buttons** - Edit, Remove, Reactivate (varies by role and status)

---

## Member Statuses

### Active (No Badge)

**What it means:**
- User has accepted invitation
- Account is fully functional
- Can log in and use platform

**Visual indicator:**
- No status badge shown
- Normal display
- Green Admin badge if they're an admin

---

### Invited (Yellow Badge)

**What it means:**
- Invitation email sent
- User hasn't accepted yet
- No access until they complete signup

**Actions available:**
- Resend invitation email
- Edit assigned role
- Remove invitation

**Common reasons:**
- User hasn't checked email yet
- Invitation in spam folder
- Email address incorrect
- Invitation expired (7 days)

---

### Suspended (Orange Badge)

**What it means:**
- Admin temporarily disabled access
- User cannot log in
- All active sessions terminated
- Data remains intact

**Actions available (Admin only):**
- **Reactivate** - Restore access immediately
- **Edit** - View/modify details
- **Remove** - Permanently delete

**Use cases:**
- Temporary leave
- Security investigation
- Quick access revocation

---

### Deleted (Red Badge)

**What it means:**
- User removed from organization
- No login access
- Soft delete (can be restored within 90 days)
- Attributed content shows as "Former Member"

**Actions available (Admin only):**
- **Reactivate** - Restore user and reassign role
- View profile details

**Note:** After 90 days, deleted users are permanently removed

---

## Inviting Team Members

### Admin-Only Feature

Only Admins can invite new members. Members and Viewers see the team list but cannot invite.

### How to Invite

1. Click **"Invite Member"** button (top right)
2. **Invitation form appears** with fields:
   - **Email Address** - Must be unique across organization
   - **Role** - Select Admin, Member, or Viewer
3. Click **"Send Invite"**
4. **Confirmation message** appears
5. **User added** to list with "Invited" status

### What Happens Next

**Email Delivery:**
- Invitation email sent to provided address
- Contains secure signup link
- Valid for 7 days

**User Signup:**
1. User clicks link in email
2. Creates password (min 8 characters)
3. Sets profile name (optional)
4. Account activates immediately

**Status Update:**
- "Invited" badge removed
- User appears as "Active"
- Can log in and use platform based on assigned role

---

### Choosing the Right Role

**Ask: What does this person need to do?**

| Need | Recommended Role |
|------|------------------|
| Manage billing and subscription | **Admin** |
| Invite/remove team members | **Admin** |
| Use AI models and chat | **Member** |
| Upload documents | **Member** |
| Sync models | **Member** |
| View reports only | **Viewer** |
| Audit usage | **Viewer** |

**Best practice:** Start with the minimum role needed. You can always promote later.

[See complete permission details →](roles-permissions.md)

---

## Changing User Roles

### Quick Role Change (Admins Only)

**Directly from team list:**
1. Find the user's card
2. Click the **role dropdown** (shows current role: Admin / Member / Viewer)
3. Select new role
4. **Confirmation dialog** appears
5. Confirm the change

**Effect:** Immediate - no logout required

---

### What Happens When Role Changes

**User experience:**
- New permissions apply instantly
- If on restricted page, sees "404 Not Found"
- New features appear in navigation
- Restricted features disappear

**Example - Member promoted to Admin:**
- Settings → Organization suddenly accessible
- Billing section appears
- Invite Member button visible
- Analytics section unlocked

**Example - Admin demoted to Member:**
- Billing section disappears (404 if navigated to)
- Cannot invite or remove users
- Organization settings hidden
- Still has full AI feature access

---

## Editing Team Members

### Edit Profile Details

1. Find the user's card
2. Click **"Edit"** button
3. **Navigates to edit page** (`/settings/organization/members/{id}`)
4. Edit available fields:
   - Name
   - Email
   - Role
5. Click **"Save Changes"**

**Note:** Changing email requires user to re-verify their account

---

### Your Own Profile

Your card is highlighted in blue with "You" badge.

**What you can edit:**
- Click **"Edit Profile"** on your own card
- Update your name and email
- Change password via password reset
- View your role (cannot change own role)

---

## Removing Team Members

### How to Remove (Admin Only)

1. Find the user's card
2. Click **"Remove"** button (appears for all non-self users)
3. **Confirmation dialog** appears:
   - "Are you sure you want to remove [Name]?"
   - "This will permanently remove them from the organization."
4. Click **"Remove User"**
5. User immediately loses access

---

### What Gets Deleted

**Immediate:**
- Organization access revoked
- Active sessions terminated
- Login blocked
- Status changes to "Deleted"

**Preserved (90 days):**
- User profile data
- Conversation history (attributed to "Former Member")
- Uploaded documents
- Activity logs

**After 90 days:**
- Permanent deletion
- Data unrecoverable

---

### Cannot Remove Yourself

You cannot remove your own account. Another Admin must remove you.

**Workaround:** Ask another Admin to remove you, or demote yourself to Member first.

---

## Viewing Deactivated Members

### Show/Hide Deactivated Button

By default, suspended and deleted users are hidden.

**To view all users:**
1. Click **"Show Deactivated"** button (top right)
2. List expands to show:
   - Active users
   - Invited users
   - Suspended users
   - Deleted users

**To hide again:**
- Click **"Hide Deactivated"**
- Only Active and Invited users show

---

## Reactivating Users

### Reactivating Suspended Users (Admin Only)

1. Click **"Show Deactivated"**
2. Find suspended user (orange "Suspended" badge)
3. Click **"Reactivate"** button
4. **Confirmation dialog** appears
5. Confirm reactivation
6. User can log in immediately

---

### Restoring Deleted Users (Admin Only)

1. Click **"Show Deactivated"**
2. Find deleted user (red "Deleted" badge)
3. Click **"Reactivate"** button
4. **Confirmation dialog** appears:
   - "Are you sure you want to restore [Name]?"
   - "This will reactivate their account and restore their access."
5. Confirm restoration
6. User restored with previous role
7. Can log in immediately

**Note:** Only works within 90 days of deletion

---

## Resending Invitations

### When to Resend

Resend invitations when:
- User didn't receive email
- Email went to spam
- Link expired (7+ days old)
- User accidentally deleted email

### How to Resend (Admin Only)

**Option 1: From invited user's card**
1. Find user with "Invited" status
2. Click **"Resend Invitation"** (if available)

**Option 2: Remove and re-invite**
1. Remove the invited user
2. Send new invitation with same email

**Effect:** New email sent with fresh 7-day link

---

## Team List Features

### Current User Highlighting

**Your own card:**
- Background: Light blue tint
- Border: Blue border
- Badge: "You" badge next to your name

**Purpose:** Quickly identify your own account in the list

---

### Role Badges

**Admin Badge:**
- Green badge
- Shield icon
- Shown next to name for active Admins

**Status Badges:**
- **Invited:** Yellow badge, "Invited" text
- **Suspended:** Orange badge, "Suspended" text
- **Deleted:** Red badge, "Deleted" text

---

### Action Buttons

**Varies by user status and your role:**

| User Status | Admin Sees | Member Sees | Viewer Sees |
|------------|------------|-------------|-------------|
| Active (self) | Edit Profile | Edit Profile | N/A |
| Active (others) | Edit, Remove, Role Dropdown | View only | N/A |
| Invited | Edit, Remove | View only | N/A |
| Suspended | Edit, Reactivate, Remove | View only | N/A |
| Deleted | Reactivate | View only | N/A |

---

## User Seat Limits

### Plan-Based Limits

| Plan | User Limit |
|------|-----------|
| Trial | 5 users |
| Starter | 5 users |
| Professional | 20 users |
| Enterprise | Unlimited |

### What Counts Toward Limit

**Counts:**
- Active users
- Invited users
- Suspended users

**Does NOT count:**
- Deleted users

---

### At Capacity

**What happens:**
- **Invite Member** button disabled
- Hover tooltip: "You've reached your plan's user limit"
- Error message if attempting to invite

**Solutions:**
1. Remove deleted/inactive users
2. Upgrade to higher plan
3. Delete old invitations (if not accepted)

---

## Best Practices

### For Admins: Security & Management

**DO:**
- Remove former employees within 24 hours
- Maintain 2-3 Admins minimum (never just 1)
- Review team quarterly
- Use Viewer role for stakeholders
- Assign minimum necessary role
- Resend expired invitations promptly

**DON'T:**
- Make everyone Admin "for convenience"
- Leave "Invited" users indefinitely
- Ignore suspended users
- Remove yourself (have another Admin do it)
- Share Admin credentials

---

### For All Users: Account Security

**DO:**
- Keep profile updated
- Use strong, unique passwords
- Report suspicious activity
- Log out on shared devices
- Verify invitation emails

**DON'T:**
- Share login credentials
- Accept unknown invitations
- Reuse passwords from other sites

---

## Troubleshooting

### Invitation Not Received

**Check:**
1. Spam/junk folder
2. Email address spelling
3. Wait 5-10 minutes (delivery delay)
4. Firewall blocking KeystoneAgentic emails

**Solutions:**
- Resend invitation
- Add `noreply@keystoneagentic.com` to safe senders
- Try different email address
- Contact support if persistent

---

### Cannot Remove a Member

**Possible causes:**
- You're not an Admin
- Trying to remove yourself
- Network connection issue

**Solutions:**
- Verify Admin role
- Ask another Admin to remove you
- Refresh page and retry
- Check internet connection

---

### Member Stuck on "Invited"

**Meaning:** User hasn't completed signup

**Reasons:**
- Didn't check email
- Email in spam
- Link expired
- Wrong email address

**Solutions:**
- Contact member directly
- Resend invitation
- Verify email address
- Check spam with user

---

### Accidentally Removed Wrong Person

**If within 90 days:**
1. Click "Show Deactivated"
2. Find deleted user
3. Click "Reactivate"
4. Confirm restoration

**If past 90 days:**
- User permanently deleted
- Must send new invitation

---

### Need to Transfer Admin Ownership

**There's no formal "owner"** - all Admins have equal permissions.

**To transfer:**
1. Promote new person to Admin
2. Optionally demote yourself to Member
3. Or keep both as Admins

---

### Lost All Admin Access

**Critical:** If all Admins are removed, organization locks.

**Prevention:** Always keep 2+ Admins

**Recovery:** Contact support@keystoneagentic.com immediately

---

## Member Privacy & Visibility

### What Team Members Can See

**All Roles See:**
- Team member names
- Email addresses
- Assigned roles
- Online status (coming soon)

**Members Cannot See:**
- Other members' usage details
- Other members' conversations
- Billing information

**Admins See Everything:**
- All member details
- Individual usage analytics
- All conversations
- Complete activity logs

---

## Frequently Asked Questions

### Can Members invite other users?

No. Only Admins can invite team members.

---

### How many Admins should I have?

**Recommended:** 2-3 Admins

**Reasoning:**
- Redundancy if one is unavailable
- Shared administrative burden
- Not so many that security is compromised

---

### Can I bulk invite users?

Not currently. Invite users one at a time.

**Coming soon:** CSV bulk upload feature

---

### Do suspended users count toward limits?

Yes. Suspended users count toward your plan's user limit.

**To free seats:** Delete suspended users instead of leaving them suspended

---

### Can one email join multiple organizations?

Yes. The same email can be a member of multiple organizations with different roles in each.

Switch organizations using the dropdown in top navigation.

---

### What happens to a user's data when removed?

**Preserved for 90 days:**
- Conversations (shown as "Former Member")
- Uploaded documents
- Activity logs

**After 90 days:** Permanently deleted

---

### Can I change my own role?

No. Only other Admins can change your role.

**Exception:** You can demote yourself from Admin to Member or Viewer

---

## Related Documentation

- **[User Roles & Permissions](roles-permissions.md)** - Detailed permission matrix
- **[Quick Start Guide](../getting-started/quickstart.md)** - Invite your first team member
- **[Profile Settings](../user-guide/profile.md)** - Manage your own account

---

## Need Help?

**Cannot invite members?**
Verify you're an Admin and within user limits

**Lost Admin access?**
Email support@keystoneagentic.com immediately

**General questions?**
Email support@keystoneagentic.com

---

**Build your team. Collaborate effectively. Manage with confidence.**

[← Back to Main Documentation](../README.md)
