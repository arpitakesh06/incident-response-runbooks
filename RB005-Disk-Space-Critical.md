# RB005 — Disk Space Critical

**Category:** Infrastructure  
**Priority:** P2  
**Version:** 1.0  
**Last Updated:** July 2025  

---

## 1. Detection Symptoms
- Monitoring alert fired for disk usage above 90%
- Application write failures or errors
- Log files not being written
- Services crashing due to insufficient disk space

---

## 2. Immediate Triage Steps
1. Confirm disk usage via monitoring dashboard
2. Identify which drive or partition is critically low
3. Check which files or directories are consuming most space
4. Verify if any services are already impacted
5. Log incident in ServiceNow with Priority P2

---

## 3. Escalation Path
| Time | Action |
|------|--------|
| 0–5 mins | L1 analyst confirms disk space issue |
| 5–15 mins | Escalate to L2 Infrastructure team |
| 15–30 mins | Escalate to Infrastructure Lead |
| 30+ mins | Notify Service Delivery Manager |

---

## 4. Resolution Procedure
1. Identify largest files and directories consuming disk space
2. Archive or delete old log files after confirming with application owner
3. Clear temporary files and application cache
4. Move large files to archive storage if available
5. Restart any services that crashed due to disk space
6. Monitor disk usage for 30 minutes post cleanup

---

## 5. Post-Resolution Validation
- Confirm disk usage is below 70%
- Verify all services are running normally
- Check monitoring alerts have cleared
- Confirm log files are being written correctly

---

## 6. Prevention Recommendations
- Set disk alert threshold at 80% for early warning
- Implement automated log rotation and archiving
- Schedule weekly disk usage review
- Set up automated cleanup jobs for temporary files
