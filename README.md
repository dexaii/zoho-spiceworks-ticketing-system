## Zoho Mail Server + Domain Hosting + Spiceworks Cloud Ticketing
**End-to-End Email Infrastructure & Helpdesk Integration Project**
# Introduction
This project demonstrates the deployment of a business email infrastructure using a custom domain and its integration with a cloud-based helpdesk system. A domain was configured with proper DNS records and linked to Zoho Mail services to establish a professional email system. The Zoho Mail account is configured with Anti-spoofing protocols and then integrated with Spiceworks Cloud Help Desk via IMAP/SMTP, enabling automatic creation of support tickets from incoming emails. The result is an end-to-end email and ticketing solution that follows basic ITIL-style workflows for handling IT support requests.
# Project Objectives
* **Deploy a Zoho-based Email System:** Set up a functional business email service using Zoho for a custom domain
* **Secure Domain & DNS Configuration:** Configure and secure DNS records (MX, TXT, SPF, DKIM, DMARC) for domain-based email deliverability and trust
* **Enable Helpdesk Integration:** Activate IMAP/SMTP access on the email account to integrate with a helpdesk ticketing system
* **Implement ITIL Workflow:** Configure the Spiceworks Cloud helpdesk with basic ITIL-style ticket management (automatic ticket creation, SLA enforcement, escalation)
* **Documentation**
# Repository Structure
The repository is organized as follows:

├── LICENSE
├── README.md
│
├── docs/
│   ├── 01-project-overview.md
│   ├── 02-domain-setup.md
│   ├── 03-zoho-mailserver-setup.md
│   ├── 04-spiceworkcloud-integration.md
│   └── 05-lessons-learned.md
│   └──screenshots/
    ├── domain/
    ├── spiceworks/
    └── zoho/
* **LICENSE:** The open-source license for this project
* **README.md:** The main README file, summarizing the project
* **docs/:** Contains detailed documentation for each phase of the project

# Key Features
### Domain Hosting & DNS Configuration
* **Domain Verification via DNS:** Added a DNS TXT record to prove domain ownership to Zoho Mail
* **MX Records for Email Routing:** Configured MX records on the domain to direct all email to Zoho Mail servers
* **Email Authentication Protocols:** Implemented SPF, DKIM, and DMARC records (the standard email authentication triad) to improve email trust and deliverability

### Zoho Mail Server Setup
* **Domain verification:** Registered the custom domain on Zoho Mail service and completed the verification process
* **Helpdesk Mailbox:** Created a dedicated support email account (help@dexaiitech.com) to be used by the helpdesk system
* **IMAP/SMTP Enabled:** Enabled IMAP and SMTP access on the Zoho mailbox, allowing external systems (like Spiceworks) to connect and send/receive emails
* **Security Measures:** Applied security settings and access controls (strong password, two-factor authentication, app-specific password for IMAP) to protect the email account

### Spiceworks Cloud Integration
* **Email Account Integration:** Connected the Spiceworks Cloud helpdesk to the Zoho Mail mailbox using IMAP settings
* **Automatic Ticket Creation:** Configured Spiceworks to automatically generate new helpdesk tickets from each incoming email to the support address
* **SLA and Ticket Workflow:** Implemented a basic SLA for response times and set up workflow rules. For example, tickets are tagged and prioritized based on keywords, and unresolved tickets auto-escalate after a certain time.
# Documentation Index
Process documentation is available in `/docs` directory:
* **Project overview:** `(docs/01-project-overview.md)` - high-level summary of the project scope
* **Domain setup:** `(docs/02-domain-setup.md)` - instructions for configuring the domain and DNS records
* **Zoho Mail server setup:** `(docs/02-domain-setup.md)` - details on setting up the Zoho Mail server, verifing domain, user and group account creation + email authentication triad
* **Spiceworks Cloud helpdesk integration:**: `(04-spiceworkcloud-integration.md)` - guidance on connecting Spiceworks to email system and setting up ticketing rules
* **Lessons learned:** `(docs/05-lessons-learned.md)` - challenges encountered and how they were resolved
# Screenshots
Configuration screenshots are stored under `docs/screenshots/` and devided into:
* **Domain & DNS settings:** TXT records, MX routing, SPF, DKIM, DMARC
* **Zoho Mail:** Domain verification, mailbox, admin console, and security settings
* **Spiceworks Cloud Helpdesk:** Email integration settings, example tickets, and workflow / SLA configuration

# Technologies Used
* **Domain Registrar & DNS Provider:** Used a custom domain and a DNS hosting service to manage DNS records (including TXT, MX, SPF, DKIM, DMARC) and interconnect to Zoho Mail services
* **Zoho Mail:** Cloud email hosting for the custom domain
* **Email security standards:** SPF, DKIM, and DMARC configurations to ensure email authenticity and deliverability
* **Email Protocols:** IMAP and SMTP for email retrieval and sending between Zoho Mail and Spiceworks
* **Spiceworks Cloud Help Desk:** SaaS ticketing system for IT support, integrated with Zoho Mail service
* **Git & GitHub:** Used version control for managing project documentation and configuration files