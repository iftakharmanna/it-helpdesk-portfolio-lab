# Ticket #005: Suspicious Account Activity

**Reported by:** Urus Medich

**Symptom:** User reported receiving a notification that their account was signed into from an unfamiliar location, despite not traveling or logging in from anywhere unusual. They are concerned their account may have been compromised.

**Investigation:** Confirmed the account was active. Reviewed recent sign-in activity and found a login attempt from an unfamiliar external IP address shortly before the user's own legitimate login. Checked whether MFA had been prompted for the unfamiliar login and confirmed it had, and that the attempt was denied since the user did not approve the MFA request. Determined the password itself may have been exposed even though MFA successfully blocked access. Given the scope of a possible credential compromise, this exceeded tier one's authority to resolve independently.

**Root Cause:** Undetermined at tier one level. Sign-in pattern was consistent with a credential-based attack attempt; MFA prevented unauthorized access, but the source of the exposed credential required deeper investigation.

**Triage and Escalation:** Classified as high priority due to potential security exposure. Immediately reset the user's password as a precaution and confirmed the user regained access with the new credentials. Escalated to the security and identity access management team for full sign-in log review, investigation into the source IP, and a determination on whether further action such as revoking active sessions or reviewing for lateral access was needed. Provided the user with guidance on password hygiene and enabling additional account monitoring while the investigation was pending.

**Resolution:** Immediate containment (password reset) completed at tier one. Full investigation and root cause determination handed off to the security and identity access management team per escalation. The ticket is closed at tier one level upon successful handoff, with the receiving team taking ownership of the ongoing investigation.

**User Communication:**
> Hi Urus, thanks for reporting this right away, that was exactly the right call. Your account itself was not accessed since the login attempt was blocked by MFA, but as a precaution, I've reset your password and you should use the new one going forward. I've also escalated this to our security team so they can investigate where this attempt came from. In the meantime, please do not approve any MFA prompts you did not personally trigger, and let me know immediately if anything else seems off.
