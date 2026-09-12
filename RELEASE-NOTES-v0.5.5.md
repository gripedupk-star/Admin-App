# EWA Android Admin v0.5.5

## Fixes
- Membership cards now expose actions according to status: Approve, Reject, Suspend, and Restore/Approve for suspended memberships.
- Membership action responses return to Memberships instead of immediately reloading WhatsApp, avoiding UI confusion.
- WhatsApp Queue now paginates with the server's `after` cursor and fetches up to 20 pages (up to 2,000 queue records per refresh).
- Opening a WhatsApp message no longer reloads the queue immediately. This prevents an OPENED item from appearing to be the only/stuck item.
- Queue cards show type, status, creation time, recipient, and message.
- Queue actions no longer clear the whole queue after each action.
- Colorful glassmorphism styling strengthened for the admin UI.
- App version updated to 0.5.5.

## Backend compatibility
Designed for EWA Core REST endpoints already present in v2.4.x:
- `/admin/app/memberships`
- `/admin/app/memberships/{id}/action`
- `/admin/app/queue`
- `/admin/app/queue/{id}/opened`
- `/admin/app/queue/{id}/sent`
- `/admin/app/queue/{id}/failed`
