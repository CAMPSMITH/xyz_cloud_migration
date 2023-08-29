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
* SAP - SAP is the current CRM.  Important customer information is retrieved from SAP for various customer portal functions
* ZenDesk - the customer portal offers helpdesk features, including connecting to helpdesk agents, ticketing and viewing ticket history.

#### Architecture
![XYZ Conceptual Architecture](images/XYZ%20Conceptual%20Arch.png)