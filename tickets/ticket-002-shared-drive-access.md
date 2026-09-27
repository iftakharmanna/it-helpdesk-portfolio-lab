# Ticket #002: Shared Drive Access Denied

**Reported by:** Hamed Naseem

**Symptom:** User reported being unable to open the Finance shared drive, receiving a permission denied message. Noted they had recently transferred to Finance and their manager confirmed they should have access.

**Investigation:** Confirmed the account was active and not locked. Checked current group memberships and found the user was not a member of the Finance shared drive access group. Reviewed recent changes and confirmed the user had been moved from Sales to Finance in the prior week, but the corresponding access group had not been updated at the time of the transfer. Confirmed with the manager that Finance drive access was expected for the role.

**Root Cause:** Department transfer was processed in the directory, but group membership was not updated to reflect the new department's required access, leaving the user without the Finance shared drive permission.

**Resolution:** Added the user to the Finance shared drive access group. Verified the user could open the folder successfully after the change took effect.

**User Communication:**
> Hello Hamed, Thanks for reporting this. I can see you were moved to Finance last week but weren't added to the Finance shared drive group at the time, which is why you couldn't get in. I've added you to that group now, so you should be able to access the folder. Let me know if you still run into any trouble.
