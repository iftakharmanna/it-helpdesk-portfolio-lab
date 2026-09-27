# Ticket #003: VPN Connectivity Issue

**Reported by:** Samuel Peters

**Symptom:** User reported being unable to connect to the VPN from home, needed to access shared drives. Noted it was working the previous day and that a restart did not resolve it.

**Investigation:** Confirmed the account was active and not locked. Checked VPN client logs and found the connection was failing at the authentication step rather than the initial connection attempt. Verified the user's password had not recently changed. Checked whether multi factor authentication was involved in the VPN login and found the user's authenticator app's time was out of sync, which was causing the issue.

**Root Cause:** Authenticator app clock drift caused MFA codes to fall outside the accepted time window, resulting in repeated VPN authentication failures.

**Resolution:** Had the user resync their authenticator app's time settings. Confirmed successful VPN connection on retest.

**User Communication:**
> Hi Samuel, thanks for flagging this. It turned out your authenticator app's clock was slightly out of sync, which made the codes get rejected during login. I had you resync it and the VPN connected successfully afterward. Let me know if it happens again.
