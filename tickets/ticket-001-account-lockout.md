# Ticket #001: Account Lockout

**Reported by:** Jammy P.

**Symptom:** User reported being unable to log into email, password rejected despite being correct, possible account lock.

**Investigation:** Verified account existed and was active. Checked lockout status and confirmed locked due to multiple failed login attempts. Reviewed recent sign-in activity for suspicious location/activity, none was found. Asked the user about other connected devices and confirmed phone's mail app had an outdated saved password causing repeated failed background login attempts.

**Root Cause:** Cached/outdated password on a secondary device (mobile mail app) triggered repeated failed authentication attempts, exceeding the lockout threshold.

**Resolution:** Unlocked the account. Had the user update the saved password on their phone's mail app. Confirmed successful login.

**User Communication:**
> Hello Jammy, Good news! Your account is unlocked and you should be able to log in now. The lockout happened because your phone's mail app had an old saved password that kept retrying in the background and eventually locked the account. I've had you update it, so this shouldn't happen again. Let me know if you run into any more trouble before your call!

**Screenshot:**
![ticket](it-helpdesk-portfolio-lab/screenshots
/image1.png)

