---
title: Secure Note Sharing
version: 1.0
last_updated: 2025-05-11
author: __Harshit Satyaseel__
audience: End User
document_type: Feature Guide
product_module: Notes > Share
---

# Secure Note Sharing

## Overview

The Secure Note Sharing feature allows users to share notes securely via an *encrypted*, time-limited link. Recipients can view the note without logging into Acme Notes.

## Use Cases

| User | Scenario | Outcome |
|------|----------|---------|
| Student | Share class notes with friend securely | Friend views note once via link |
| Manager | Send meeting notes to client quickly | Client views notes via link (no login needed) |
| Researcher | Share sensitive draft securely | Link expires after 24 hours, ensuring safety |
| Admin | Has all the administrative rights to approve the share | Anytime |

## How to Share a Secure Note

### Steps

1. Open **Acme Notes** and navigate to the note you want to share  
2. Click **Share → Secure Link**  
3. Select **Link Expiry Option**:  
   - 24 hours  
   - 1 view  
4. Click **Generate Link**  
5. Copy the generated link and share it via email/message  
6. To revoke the link, click **Revoke Link**

## Reference Code Example

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

//dummy references

Here are some of the useful reference materials to learn more. 

- Acme Notes Security Policy
- API Docs: Share Link Endpoint
- User Guide: Managing Notes





