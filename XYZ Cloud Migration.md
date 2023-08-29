# XYZ cloud migration engagement

## About XYZ
XYZ is an enterprise with traditional on-premise infrastructure, applications and products that is interested in moving to the cloud as well as modernizing their product suite and architecture. Of late, their customer facing portal has been particularly problematic for XYZ.  XYZ's IT department is looking to initially migrate their customer facing portal to the cloud and then later on, scale the effort across the rest of enterprise. 

### Pain Points
* Long lead times to provision new environments
* Long lead times and cycles for development
* Lack of consistency between their environments
* Downtime during deployments
* Code quality issues in production releases

### Considerations and Constraints
* XYZ does not want any interruptions of service during deployment or migration
* XYZ does not have any internal skillset with cloud
* XYZ does not have bandwidth to rearchitect and modify existing systems for cloud migration
* XYZ is willing to learn skills needed to maintain and operate systems after cloud migration

### Opportunities
* containerization
* modernization

## XYZ Customer Portal
XYZ's customer portal is a complex enterprise portal that has been in operations for many years and is a critical system for XYZ.  As part of the cloud migration, the company would like to ensure that the pain points are addressed.  They would also like to modernize the infrastructure and architecture of the solution to reduce maintenance overhead and also add in capabilities that improve security posture.

### Customer Portal Current
#### Components
Based on initial discussions with XYZ, the customer portal is a traditional enterprise n-tier architecture.  
* Clustered J2EE application servers
* Static content
* Database

#### Key integrations
The customer portal has integrations that are critical to the customer portal
* SAP - SAP is the current CRM.  It is on-prem. Important customer information is retrieved from SAP for various customer portal functions
* ZenDesk - the customer portal offers helpdesk features, including connecting to helpdesk agents, ticketing and viewing ticket history.

#### Current Conceptual Architecture
![XYZ Conceptual Architecture](images/XYZ%20Conceptual%20Arch.png)

### Customer Portal Cloud Migration
The proposal is to migrate XYZ's customer portal to the cloud.  Migrating the customer portal to the cloud will include minor re-architecting of the system to better fit the cloud environment, reduce operational overhead, improve system resiliency and recovery. 

#### Guiding Principles
* Maximize use of cloud vendor services, prefer these over manually installed or managed services, when possible in order to reduce development and operational effort
* Use containers to ensure consistency between environments
* Use CI/CD automation to reduce operational overhead associated with deployments and to eliminate downtime during deployments
* avoid down time
* Minimize changes to the application to reduce risk and cloud migration duration

#### Areas requiring special migration planning
* Database migration
* DNS updates and cutover

#### Migration Phases
To minimize risk and downtime, migration will be handled in phases

1. **Phase 1 - Web Server & Application Server Migration**
1. Phase 2 - DNS Cutover
1. Phase 3 - On-Prem Web Server & Application Server Retirement
1. Phase 4 - Database Cutover

#### Proposed Phase 1 Interim State Conceptual Architecture
![XYZ Interim Architecture](images/XYZ%20Conceptual%20Arch%20-%20Proposed.png)
![XYZ CI/CD](images/XYZ%20CI%20CD%20-%20Proposed.png)
Notes: 
* Deployment pipelines to include unit testing, static code analysis, and static application security testing (SAST) 
* Depending on workflow, pipelines can either be environment specific or be configured to deploy to all environments in progression.  

#### Phase 1 Engagement Model
Phase 1 is tailored to address the pain points.
* Containers are used to ensure consistency between environments
* IAC and deployment automation can significantly reduce time required to provision new environments
* Container orchestration and deployment automation can eliminate downtime during deployments
* Integrating unit testing and static code testing into deploymet automation can improve code quality
* Deployment automation can reduce lead times and development cycle times
![XYZ CI/CD](images/XYZ%20Migration%20Engagement.png)

Other phases to be planned after phase 1 is completed.