# RB006 — Login Failure Spike

**Category:** Security  
**Priority:** P1  
**Version:** 1.0  
**Last Updated:** July 2025  

---

## 1. Detection Symptoms
- Monitoring alert fired for high volume of failed login attempts
- Users reporting unable to log in
- Authentication service showing errors
- Possible brute force or credential stuffing attack detected

---

## 2. Immediate Triage Steps
1. Confirm login failure spike via monitoring dashboard
2. Check if failures are from specific IP addresses or distributed
3. Identify if legitimate users are also affected
4. Check authentication service health and error logs
5. Log incident in ServiceNow with Priority P1

---

## 3. Escalation Path
| Time | Action |
|------|--------|
| 0–5 mins | L1 analyst confirms login failure spike |
| 5–10 mins | Escalate to L2 Security team |
| 10–20 mins | Escalate to Security Lead |
| 20+ mins | Notify Service Delivery Manager and CISO |

---

## 4. Resolution Procedure
1. Check authentication logs for source of failures
2. If brute force detected — block suspicious IP addresses immediately
3. If auth service issue — restart authentication service
4. If SSO or token issue — rotate tokens and restart SSO service
5. Unlock any legitimate user accounts that got locked out
6. Monitor login success rate for 30 minutes post fix

---

## 5. Post-Resolution Validation
- Confirm login success rate is back to normal
- Verify no suspicious IP addresses still active
- Check authentication service is running normally
- Confirm locked out users can log in successfully

---

## 6. Prevention Recommendations
- Implement multi-factor authentication for all users
- Set account lockout after 5 failed attempts
- Configure IP-based rate limiting on login endpoint
- Set up real-time alerting for login failure spikes above baseline
