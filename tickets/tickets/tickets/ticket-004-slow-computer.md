# Ticket #004: Slow Computer Performance

**Reported by:** Nathan Diaz

**Symptom:** User reported their laptop running noticeably slower than usual, with programs taking longer to open and occasionally freezing.

**Investigation:** Checked system resource usage remotely and found CPU and memory consistently near capacity even with few applications open. Reviewed startup programs and found several unnecessary applications launching automatically at boot. Checked for pending Windows updates and found multiple updates had failed to install over several weeks, leaving background update processes repeatedly retrying and consuming resources. Ran a basic malware scan as a precaution, which came back clean.

**Root Cause:** A backlog of failed Windows updates was causing background processes to repeatedly retry installation, consuming CPU and memory and slowing overall system performance, compounded by unnecessary startup programs.

**Resolution:** Disabled unnecessary startup applications. Manually resolved and installed the pending Windows updates. Restarted the machine and confirmed performance returned to normal.

**User Communication:**
> Hi Nathan, thanks for reporting this. Your laptop had a backlog of Windows updates that weren't installed properly, which was using up a lot of background resources, along with some startup programs that didn't need to run automatically. I've fixed both, and performance should be back to normal now. Let me know if it slows down again.
