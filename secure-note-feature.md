---
Title: Secure Note Sharing
Version: 1.0
Last_updated: 2025-05-11
Author: Harshit Satyaseel
Audience: End User
Document_type: Feature Guide
Product_module: Notes > Share
---

# Secure Note Sharing

## Overview

The Secure Note Sharing feature allows users to share notes securely via an encrypted, time-limited link. Recipients can view the note without logging into Acme Notes.

## Use Cases

| User | Scenario | Outcome |
|------|----------|---------|
| Student | Share class notes with friend securely | Friend views note once via link |
| Manager | Send meeting notes to client quickly | Client views notes via link (no login needed) |
| Researcher | Share sensitive draft securely | Link expires after 24 hours, ensuring safety |

## How to Share a Secure Note

1. Open **Acme Notes** and navigate to the note you want to share  
2. Click **Share → Secure Link**  
3. Select **Link Expiry Option**:  
   - 24 hours  
   - 1 view  
4. Click **Generate Link**  
5. Copy the generated link and share it via email/message  
6. To revoke the link, click **Revoke Link**

## Code Example

```javascript
// Generate secure share link for a note
const generateSecureLink = (noteId, expiryType) => {
  const token = encryptNote(noteId);
  const link = `${BASE_URL}/shared/${token}?expiry=${expiryType}`;
  return link;
}

// Example usage
const link = generateSecureLink('note123', '24h');
console.log('Shareable link:', link);
```

## References

Below are more reference materials to learn more.

// dummy reference

- Reference 1
- Reference 2
- Reference 3
