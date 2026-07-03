# RB004 — SSL Certificate Expiry

**Category:** Security  
**Priority:** P2  
**Version:** 1.0  
**Last Updated:** July 2025  

---

## 1. Detection Symptoms
- Browser showing "Your connection is not private" warning
- HTTPS requests failing with SSL error
- Monitoring alert fired for certificate expiry
- Users unable to access website or application

---

## 2. Immediate Triage Steps
1. Confirm SSL certificate expiry date via browser or monitoring tool
2. Check if expiry has already occurred or is imminent
3. Identify which domains and services are affected
4. Notify affected teams and stakeholders immediately
5. Log incident in ServiceNow with Priority P2

---

## 3. Escalation Path
| Time | Action |
|------|--------|
| 0–5 mins | L1 analyst confirms certificate expiry |
| 5–15 mins | Escalate to L2 Security or Infrastructure team |
| 15–30 mins | Escalate to Security Lead |
| 30+ mins | Notify Service Delivery Manager |

---

## 4. Resolution Procedure
1. Generate new SSL certificate from certificate authority
2. Validate new certificate before deployment
3. Deploy new certificate to web server
4. Restart web server service after deployment
5. Confirm HTTPS is working correctly on all affected domains
6. Update certificate expiry date in monitoring tool

---

## 5. Post-Resolution Validation
- Confirm browser shows padlock icon and no warnings
- Verify HTTPS requests are completing successfully
- Check monitoring alerts have cleared
- Confirm new certificate expiry date is set correctly

---

## 6. Prevention Recommendations
- Set up automated SSL certificate renewal using certbot
- Configure monitoring alerts 30 and 60 days before expiry
- Maintain a certificate inventory with expiry dates
- Schedule quarterly review of all SSL certificates
