# Bug Report: Chat Not Syncing Between Mobile and Desktop App

**ID:** BUG-CLAUDE-001  
**Severity:** Major  
**Priority:** High  
**Status:** Reported to Anthropic  
**Reporter:** Marina Pushkareva  
**Date:** 2026-06-10  

---

## Summary
Chat messages do not sync between the Claude iOS mobile app and the Claude Windows desktop application. Additionally, messages disappeared completely from both platforms.

## Environment
- Desktop: Claude Windows native app (not browser)
- Mobile: Claude iOS app
- OS: Windows 11
- Connection: Stable Wi-Fi

## Steps to Reproduce
1. Open an active chat in the Claude mobile app
2. Open the same chat in the Claude Windows desktop app
3. Send new messages via mobile
4. Close and reopen the Claude Windows desktop app
5. New messages from mobile are not displayed

## Expected Result
Chat history syncs automatically across all devices. New messages appear after reopening the app.

## Actual Result
- New messages do not appear in desktop app after restart
- Some messages disappeared completely from both mobile and desktop versions
- Only workaround: log out and log back in
- Issue occurred multiple times

## Anthropic Support Response
Anthropic confirmed that regular Claude Desktop chats do not sync across devices by design. However, they acknowledged that message disappearance from both platforms simultaneously is a separate, more serious issue related to chat persistence.

## Workaround
Log out and log back in to force sync. Use Cowork Dispatch feature for cross-device syncing.

## Attachments
- ![Screenshot 1 - Desktop and Mobile out of sync](https://github.com/marinapushkareva1312/qa-portfolio/blob/main/bug-reports/IMG_9519.PNG)
- ![Screenshot 2 - Anthropic response 1](https://github.com/marinapushkareva1312/qa-portfolio/blob/main/bug-reports/IMG_9520.PNG)
- ![Screenshot 3 - Anthropic response 2](https://github.com/marinapushkareva1312/qa-portfolio/blob/main/bug-reports/IMG_9521.PNG)
- ![Screenshot 4 - Bug report sent](https://github.com/marinapushkareva1312/qa-portfolio/blob/main/bug-reports/IMG_9522.PNG)
- ![Screenshot 5 - Message disappearance]()
- Anthropic support conversation ID: 215474634353141
