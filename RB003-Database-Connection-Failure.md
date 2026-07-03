# RB003 — Database Connection Failure

**Category:** Database  
**Priority:** P1  
**Version:** 1.0  
**Last Updated:** July 2025  

---

## 1. Detection Symptoms
- Applications returning database connection timeout errors
- Services reporting inability to connect to database
- Monitoring alert fired for database unreachable
- Users seeing error pages or failed transactions

---

## 2. Immediate Triage Steps
1. Confirm database is unreachable by checking monitoring dashboard
2. Attempt to connect to database manually from application server
3. Check database server CPU, memory and disk usage
4. Verify connection pool status and available connections
5. Log incident in ServiceNow with Priority P1

---

## 3. Escalation Path
| Time | Action |
|------|--------|
| 0–5 mins | L1 analyst confirms DB connectivity issue |
| 5–10 mins | Escalate to L2 Database Administrator |
| 10–20 mins | Escalate to Database Lead |
| 20+ mins | Notify Service Delivery Manager and affected teams |

---

## 4. Resolution Procedure
1. Check if database service is running — restart if stopped
2. Check connection pool size — increase if exhausted
3. Review database logs for errors or locks
4. Kill any long running queries blocking connections
5. Restart application services after database is confirmed stable
6. Verify all application services can connect successfully

---

## 5. Post-Resolution Validation
- Confirm database is accepting connections
- Verify application services are running normally
- Check monitoring alerts have cleared
- Confirm with users that transactions are completing successfully

---

## 6. Prevention Recommendations
- Set connection pool size based on peak traffic analysis
- Implement database connection monitoring with alerts
- Schedule regular database health checks
- Set up read replicas to distribute connection load
