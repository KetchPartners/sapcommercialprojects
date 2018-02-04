---
layout: default
title: Scrum Sprint 2 Customer Opportunity to CPQ Quotation
comments: true
# other options
---
## Sprint 2 

### Process Flow: Customer Opportunity CRM to Project Estimate

|Trigger                                         | Process End                                              | 
|:-----------------------------------------------|:---------------------------------------------------------|
|Customer Opportunity for Project Product(s).    |Project Estimate Approved and Passed to CPQ               |

### Technical Components
- SAP Commercial Project Management
- SAP Customer Relationship Management - Hybris
- SAP CPQ Quotation Management
- SAP HANA S/4
- SAP HANA Data Services API's (ODATA / REST / Data Streaming)
- SAP Orchestrator Workflow and Rules Engine
- SAP Fiori
- Agnostic Web Apps running on HANA XSA
- Third Party Intefaces to be determined.

### Integration
The following other processes are impacted by this process:
- Customer Opportunity Processing
- Customer Quotation Review and Approvals
- Baseline Planning
- Human Resource Employee Master
- Network LDAP / SAP Single Sign-on
- Customer Portal (DMZ Zone)

### Process Components
- CRM Opportunity Has Trigger to Initiate Workflow to Start CPM and Project Estimate
- Workflow (Sales > Project PMO > Assign Project Manager > PM Estimate > Approval > Sent Estimate to Opportunity)
- Launch Pad Role Based Worklists
- Desktop Notifications
- Workflow Email with Ability to Process Workflow Step
- Exception alerts, with follow up action
- Project estimate models and level of detail
- Project estimates will use Analysis Office Excel, Excel in SAP to do planning.
- Probability of success used as criteria for priortization.
- Ability from opportunity link and view CPM project estimate details.
- Multiple estimate versions
- Master project before a real sales has been made, to avoid clutter in S4 system.
- Establishment of Estimate Baseline Available as CO plan version in S4.
- Process supporting reporting requirements.
- Project team roles.
- Project security and authorizations requirements.


### Decisions Required
- What field in CRM to trigger the workflow process
- What details of plan to pass back to opportunity (key figure can be summarized amount from estimate)
- What is the rules of the workflow and variants for small vs larger projects.
- Match business roles to CPM roles
- What of process will show up in dashboards, and other "to do" worklists.
- What CPQ needs and how will it trigger the CPQ Quotation phase?  Can the creation of the quote be automated?

### In Progress Prototype and Process Flow

[Process flow diagram is available at this link.](https://28syaa.axshare.com/#g=1&p=process_flow)
<br />
#### Process Flow Instructions
Click on the process flow boxes to see sample prototype screen.

#### Password to Process Flow
Please email [Mateo Carlos](mailto:mcarlos@ketch.partners) for password as process flows contain KM specific information.

#### Process Flow Standards
The process flows follow BPMN open source standard format [BPMN](https://BPMN.io).  BPMN is code based using XML standardized format.  BPMN can be used to facilitate coding items like workflow, and BPMN can be used to faciliate automated testing.
Click on DISCUSS in left panel to add comment or add comment or question below.  Keep questions about the software, for KM specific information please email [David Beach](mailto:dbeach@ketch.partners) or [Chris York](mailto:cyork@ketch.partners)

### Reference Material

[SAP Help Portal - SAP S/4HANA Commercial Project Management] (https://help.sap.com/viewer/0cb2ca60abdd42978337e0622f1c211f/1610%20002/en-US)
