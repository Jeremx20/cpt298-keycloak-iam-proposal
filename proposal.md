# Project Proposal

## 1. Project Identification

•    Project Title: Keycloak IAM Solution
•    Course: CPT 298
•    Term: Summer 2026
•    Student Name(s): Jeremie Onanga, Theodore (Teddy) Robillard
•    Primary Contact:
•    Proposed Start Date: 06/04/2026
•    Proposed End Date: 07/05/2026

---

## 2. Project Selection & Motivation

Describe why you selected this project and why you are a good fit.
Include:
•    Personal or professional motivation
•    Alignment with career goals
•    Relevant interests or prior exposure
Project topic was suggested by Jeremie, and he has an interest in cybersecurity. 
Theodore has a background in networking. 

---

## 3. Problem Statement
cpt.internal lacks centralized IAM—each service manages its own accounts independently. This forces users to maintain separate credentials for every tool, makes provisioning and deprovisioning error-prone, prevents centralized auditing, and blocks consistent security policies. All cpt.internal users (students, instructors, admins) are affected. This fragmentation increases security risk, wastes operational resources, prevents students from learning enterprise IAM practices, and doesn't scale. Deploying a unified IAM solution like Keycloak addresses these gaps by centralizing authentication, enabling consistent policies, and providing comprehensive audit trails.

---

## 4. Proposed Solution Overview
We will deploy Keycloak as the centralized IAM solution for cpt.internal. It will act as the Identity Provider (IdP) for one integrated service, enabling SSO via OpenID Connect.
Core features
SSO for one internal service via OIDC
Centralized user/group management in a dedicated realm
Role-Based Access Control (RBAC)
Strong authentication policies (passwords, brute-force protection, sessions)
Audit logging
HTTPS via reverse proxy + TLS
PostgreSQL backend
Security audit (config review + automated scan)
Documentation in UVDesk and deployment guide
Explicit exclusions
LDAP/AD deployment from scratch
Self-service password reset
Modification of integrated services
Manual penetration testing of integrated services beyond the configuration audit
and as a stretch goal to implement MFA


## 5. Technical Stack & Tools

OS: Linux on cpt.internal VMs
Languages: Bash for scripts; Python for optional automation
Frameworks: Keycloak (container or distribution)
Database: PostgreSQL
Infrastructure: Docker, reverse proxy (Nginx or Caddy)
Tools: Git/GitHub, GitHub Issues, UVDesk, Discord, Keycloak admin console + REST API
For audit: OWASP ZAP, testssl.sh, nmap, Keycloak hardening guide


## 6. Prerequisite Knowledge & Skills
Jeremie Onanga:
Skills I already have

Linux system administration (Debian, Ubuntu, Arch), Cisco networking fundamentals (VLANs, ACLs, OSPF, NAT, EtherChannel), Python and Bash scripting, penetration testing basics,...
Skills I need to learn

OAuth 2.0 and OpenID Connect (authorization code flow, PKCE), SAML 2.0, JWT (structure, validation, attacks), Keycloak administration (realm setup, client configuration, policies, federation), LDAP basics, CVSS scoring.

Relevant coursework

CPT 201 (Linux administration), CPT 239 (Cisco networking), CPT 271 (Network Security), CPT 281 (Penetration Testing).
Prior projects
 Arch Linux Local AI Services Station (Ollama, Docker, systemd services), CPT 281 lab work.


 Teddy Robillard:
 
 Skills I have: 
  Linux skills (Debian), Cisco networking fundamentals (VLANs, ACLs, OSPF, NAT, EtherChannel), and Python and Bash scripting

 Skills I need: 
  OAuth 2.0 and OpenID Connect (authorization code flow, PKCE), SAML 2.0, JWT (structure, validation, attacks), Keycloak administration (realm setup, client configuration, policies, federation), LDAP basics, CVSS scoring.

---

## 7. Project Scope & Deliverables
MVP
Keycloak deployed with PostgreSQL and HTTPS
One realm configured with users, roles, and policies
One service integrated via OIDC, end-to-end validated
Audit logging enabled
Security audit report (config review + automated scan)
Documentation: README, deployment guide, UVDesk articles, admin runbook

Required outputs
GitHub repository
UVDesk articles
Security audit report
Final presentation

Stretch goals 
MFA (TOTP) for admin accounts
Second service integration
LDAP/AD federation (if existing directory available)


## 8. Milestones & Timeline
Provide a rough timeline broken into phases.

Example:
- Phase 1: Research & Design
- Phase 2: Core Implementation
- Phase 3: Testing & Refinement
- Phase 4: Documentation & Presentation

Dates do not need to be exact, but planning is required.

---

## 9. Risks, Constraints & Dependencies
Identify potential challenges.

Include:
- Technical risks
- Time constraints
- External dependencies (APIs, credentials, access)
- Mitigation strategies

---

## 10. Security, Ethics & Safety Considerations
Address any relevant concerns, such as:
- Authentication and authorization
- Data sensitivity
- Network exposure
- Logging, monitoring, or automation impact
- Ethical considerations

A brief assessment of all of these is required, even if it is "N/A".

---

## 11. Team Structure (If Applicable)
If working in a group, describe:
- Team roles
- Communication plan
- Conflict resolution approach
- Workload distribution

---

## 12. Documentation & Knowledge Transfer Plan
Explain how this project will be documented.  Please note that this should include documentation in the UVDesk knowledgebase at the very least.  Programming projects should include readme.md files. 

Include:
- README or user documentation
- Deployment or maintenance guides
- How another student or administrator could continue the project

---

## 13. Faculty/cpt.internal Resources Requested
List any required resources:
- VM access
- Network access
- Credentials or APIs
- Special permissions
- Hardware (if applicable)

Please be sure to consider any future tickets you may need to submit to complete this work as those will need to be generated and assigned to the appropriate groups as soon as feasibly possible once the project kicks off to ensure timely delivery.  I will step in to help where required but you will likely be working with students in other classes so please be cognizant of their time!

---

## 14. Acknowledgement of Expectations
By submitting this proposal, I acknowledge that:
- This is a self-directed technical project
- I am responsible for research and troubleshooting
- Evaluation will consider process, documentation, and professionalism

**Signature (Name & Date):**

Student 1:  ____________________________ Date: _______________
Student 2:  ____________________________ Date: _______________
Student 3:  ____________________________ Date: _______________
Student 4:  ____________________________ Date: _______________

Instructor: ____________________________ Date: _______________
