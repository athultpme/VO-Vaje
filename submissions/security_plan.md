# Security Improvement Plan - GreenFields Food Processing Ltd
Company size: 120 employees
Budget: 80,000 Euro/year
Timeframe: 12-18 months

## 1. Security Maturity Assessment
     GreenFields currently operates at a low security maturity level. The organization lacks formal risk assessments, documented policies, and security monitoring. Shared administrator credentials, unsegmented networks, and inconsistent patch management expose the company to sign there significant cyber risks. Employees are untrained, backup are stored on the same network, and there is no incident response plan. The environment is typical of a small to medium organization with minimal cybersecurity investments.

## 2. Top 10 Security Risks

1.	Unsegmented Network: Production systems are on the same LAN as corporate networks, increasing the risk of lateral movement during an attack.
2.	Shared Administrator Credentials: Compromised admin accounts can lead to full systems takeover.
3.	Weak Password Policies: Default or reused passwords increase the risk of credential theft.
4.	No Multi-factor Authentication (MFA): Remote access, email, and cloud services are vulnerable to phishing.
5.	Inadequate Backup Strategy: Backups stored on the same network are vulnerable to ransomware.
6.	No Security Monitoring: alack pf SIEM or logging tools delays incident detection.
7.	No Incident Response Plan: Recovery after a breach will be slow and disorganized.
8.	Unpatched Systems: Outdated software and endpoints increase vulnerability to exploits.
9.	Phishing and Social Engineering: Untrained employees are susceptible to credential theft.
10.	Lost Devices: Laptops and smartphones without encryption or remote wipe can leak sensitive data.

## 3. Priority Security Improvements

### Policy and Governance
1. **Develop Security Policies (3-6 months)**
•	- Create an **Acceptable Use Policy (AUP)**, **Password Policy**, **Remote Access Policy**, and **Incident Response Plan (IRP)**.
•	- **Importance:** Establishes clear rules and accountability for security practices.

2. **Formalize Risk Assessment (3-4 months)**
•       - Perform a risk assessment using a lightweight framework (eg, NIST CSF or ISO 27001 Lite).
•	- **Importance:** Identifies critical assets and prioritizes risks.

---

### Technical Controls

3. **Implement Network Segmentation(6-12 months)**
•	- Isolate **production network** from corporate LAN using VLANs and firewall.
•	- **Importance:** Prevent lateral movement in case of a breach.

4. **Enforce Strong Password And Multi-factor Authentication(0-3 months)**
•       - Require complex passwords and **MFA for all critical accounts** (email, VPN, cloud services).
•	- Use a password manager for employees.
•	- **Importance**: Reduces credential theft and phishing effectiveness.

5. **Improve backup and recovery (3-6 months)**
   - Apply the **3-2-1 backup rule**: 3 copies, 2 media types, 1 offsite (e.g., cloud or air-gapped storage). Regularly test restores.
   - **Importance:** Ensure availability and resilience against ransomware and data loss.

6. **Enable security monitoring (6-12 months)**
   - Implement **Microsoft Defender for Endpoints** (or a lightweight SIEM?EDR) with centralized logging and alerts for critical systems.
   - **Importance:** Reduces the window of exposure to known vulnerabilities.

7. **Automate patch management (ongoing, starting 3-6 months)**
   - Use built-in tools (WSES, Microsoft Intune, or similar) to automate updates for windows, M365, ERP, and warehouse systems.
   - **Importance:** Reduces the window of exposure to known vulnerabilities.


### Organizational and Training Measures

8. **Security awareness training and phishing simulation (0-3 months, then quarterly)**
   - Conduct short, role-specific training plus **regular phishing simulation** (e.g., quarterly). Measure click-through rates.
   - **Importance:** Human error is a major risk; training reduces phishing success and improves reporting.

9. **Develop and test an incident response plan (IRP) (6-12 months)**
   - Define roles, communication channels, and playbooks for **ransomware**, **phishing**, and **data-loss incidents**; run tabletop exercises.
   - **Importance:** Minimizes downtime, financial loss, and reputational damage after a breach.
   
10. **Implement least-privilege access (3-6 months)**
   - Remove unnecessary admin rights; grant elevate privileges only to essential staff using **role-based access control (RBAC)**.
   - **Importance:** Limits the impact of compromised accounts and insider threats.

---

## 4. Implementation Roadmap

### Phase 1 - Immediate (0-6 months)

| Activity | Timeline |
| --- | --- |
| Define basic security policies (AUP, Password, Remote Access) |Month 1-3 |
| Roll out MFA for all users (email, VPN, M365, ERP) | Month 1-3 |
| Launch security awareness training and first phishing simulation | Months 1-3 |
| Improve backup strategy (3-2-1 rule, test restores) | Months 3-6 |
| Inventory all assets (users, devices, systems, data flows) | Month 1-3 |


### Phase 2 - Medium-term (6.12 months)
| Activity | Timeline |
| --- | --- |
| Implement network segmentation (VLAN, firewall rules) | Months 6-12 |
| Deploy security monitoring (Defender for Endpoints / SIEM) | Month 6-12 |
| Automate patch management | Months 6 and ongoing |
| Perform formal risk assessment | Months 3-6 |
| Review and refine access controls (least privilege) | Month 6-12 |


### Phase 3 - Strategic (12-18 months)

| Activity | Timeline |
| --- | === |
| Finalize and exercise incident response plan | month 12-18 |
| Implement RBAC and refine user roles | Month 12-18 |
| Review and update all policies for compliance (e.g., GDPR) | Month 12-18 |
| Begin supplier-security assessments (e.g., their ransomware history) | Months 12-18 |

---
 
## 5. Estimated Budget Allocation (80,000/year Euro)

| Category | Estimated allocation | Notes |
| --- | --- | -- |
| Security tools (MFA, EDR/SIEM, VPN, firewall rules) | 30,000 Euro | Prefer cloud-based or built-in tools (e.g., Microsoft Defender).
| Training and awareness (training platform, simulation, workshops) | 15,000 Euro | Focus on measurable phishing-simulation service and e-learning. |
| External consulting (risk assessment, IRP, architecture review) | 20,000 Euro | Use part-time consultants to assist the small internal IT team.
| Infrastructure improvements (backup storage, minor network upgrades) | 15,000 Euro | Focus on non-disruptive changes (e.g., additional backup storage). 

## 6. Metrics for Measuring Security Improvement

Management should track these 5 key security metrics (KPIs) quarterly:

1. **Phishing click rate** - Percentage of employee who click on test phishing emails. Goal: decrease over time.
2. **Patching compliance** - Percentage of endpoints and servers patched within 30 days of release. Goal: >= 90%.
3. **Backup success rate** - Percentage of scheduled backups that complete successfully. Goal: >= 99%.
4. **Incident response time** - Mean time from detection to containment of a confirmed incident. Goal: reduce quarter-on-quarter.
5. **Policy compliance** - Percentage of employees who complete required security training and pass knowledge checks. Goal: >=95%.

---

This plan is designed to be **practical** for a small IT team, fit within the **80,000/year Euro budget**, and be implemented within **12-18 months** while minimizing production disruption.






