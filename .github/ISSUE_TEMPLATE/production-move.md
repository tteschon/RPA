---
name: Production Move
about: Describe this issue template's purpose here.
title: Prod Move
labels: ''
assignees: ''

---

Prod move for [NAME] Automations.

**_[NAME] Move To Production Checklist_**
- [ ] Active Directory Bot Account Created (svc_botaccount) 
- [ ] Provision Bot Account for Jira Access
- [ ] Provision Bot Account for SalesForce Access
- [ ] Prod SMTP Account (svc_GSrpauser) is this okay to use or do we need to provision new Prod SMTP.)
- [ ] Production Bot Runner Machine per Automation (1 Dispatcher, 1 Performer)
- [ ] Production Folder - Folder Structure For New Tenant

### **QA To Prod Code Push**
To meet [NAME] governance recommendations in Prod we will export package and manually add the package to the Prod Tenant

- [ ] Dev. Export Viasat Dispatcher Package
- [ ] Dev. Export Viasat Portal Reset Package
- [ ] Admin. Import (Add Package) on Production Tenant (Will Require Account in Prod With Perms, Can Be Anyone)
- [ ] Admin. Add Package To Production Folder (Will Require Account in Prod With Perms, Can Be Anyone)
     - If Production Folder Does Not Exist In Prod Tenant Create One.

**_Assets_**
Assets will need to be provisioned and then created inside of the Production Orchestrator Environment. 
- [ ] Prod SalesForce Credentials
- [ ] Prod SalesForce Consumer Credentials
- [ ] Prod SalesForce Security Token
- [ ] Prod SalesForce Server URL
- [ ] Prod Jira_API_Token
- [ ] Prod Jira_App_Cred
- [ ] Prod Jira_PAT (Personal Access Token)
   - Login to Jira
   - Go to Profile
   - Personal Access Tokens
   - Create Name
   - Create Expiration Date
- [ ] Prod Jira_Server
- [ ] Dispatcher_Email_Distro
- [ ] EmailDistro_Portal_Reset


### **Queue Creation**
Queues will need to be created in Orchestrator because we are utilizing the RE-Framework, particularly the dispatcher/performer model. Two queues will need to be created prior to the execution of the automation.

- [ ] [NAME] Queue Created in Prod

---

## Open Questions
