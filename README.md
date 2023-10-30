---
description: User manual
---


# Primo RPA

Welcome to Primo RPA user manual

![](<.gitbook/assets/Primo-Logo.png>)

**Primo RPA** is a Russian software solution for robotization of business processes.

Benefits of using Primo RPA:
* Cost reduction by employing robots to perform repetitive routine operations.
* Performance improvement by having the robots do the operations faster, which increases profits and ensures customer loyalty. 
* Quality improvement by reducing the number of human/operator errors.

## System components
Primo RPA system includes the following components: Primo RPA Studio, Primo RPA Robot, Primo RPA Orchestrator and Primo RPA Idea Hub..

## Functionality

### Primo RPA Studio

Primo Studio is the main tool for robot development. This is where analysts and developers create RPA scenarios by using built-in and custom-made components. 

Key features:
1. Creating scenarios for robots. Scenarios can be developed as a sequence of operations, as a diagram or as code, which makes it possible to robotize scenarios of virtually any complexity. A set of scenarios constitutes an RPA project, within which scenarios can be grouped into folders. 
2. Scenario debugging. It is a method of testing a scenario via Studio and tracking in console the results of its execution. Debugging provides a way to analyze and fix errors in scenarios before the project is published.
4. Dependencies. It is possible to use additional libraries while working with an RPA project. Another useful tool is the ability to develop, publish and use your own custom libraries in RPA projects.
5. Project templates. A project can be turned into a template that will then be used to create new projects. 
6. Search templates. These templates are used to interact with the UI of applications. They allow identifying a specific component of an application to gain programmatic access to it. 
7. Scenario recording. To facilitate scenario creation, user actions can be recorded.
8. Traffic logging. Logs simplify analysis of traffic exchange with portals, websites and web services,  and help create Web requests in scenarios based on the available data.
9. Import of projects. Using this functionality you can import into Studio projects from other RPA platforms, such as UiPath and Blue Prism.
10. Integration with Orchestrator. This feature allows you to get Studio licenses through Orchestrator, as well as publish the finished projects in Orchestrator..

### Primo RPA Robot

Primo Robot is a robot that executes scenarios assigned by the user. It supports working both in Windows and in Linux environments, which is especially important for the companies that are actively using Linux-based systems.

Primo Robot application is accessible through the command line as well as the GUI. Working through the GUI is done by using the Primo Robot Runner utility that is included in the distribution package. It is also possible to manage robots from within Orchestrator - that capability is covered in more detail in the Primo Orchestration section below. 

**Primo Robot features**:
1. Manual launching of RPA project execution. 
3. Integration with Orchestrator. Functionality for data exchange with Orchestrator.
4. Logging (logs and user events). 

**Primo Robot Runner utility**:
1. Provides a GUI that facilitates working with Primo Robot.
2. Automatic launching of tasks for execution or RPA projects. Tasks can be set to launch automatically in accordance with a schedule. 
4. Working with workstations. Basic functionality for managing RDP sessions.

### Primo RPA Orchestrator 

Primo Orchestrator is a software product that automates launching of RPA projects on multiple robots deployed within an organization, as well as provides the means to manage robots. Orchestrator can be used to set a schedule for robots and track their work. For large companies that have multiple separate groups of users, Orchestrator provides a way to “isolate” robot groups from each other by supporting multi-tenancy. That means that users from each group can only see and manage their group’s robots, and cannot affect the robots from other groups.

Key features:
1. Centralized management of licenses for Primo RPA products. Obtaining and setting up licenses for selected products, managing them via Orchestrator interface. 
2. Centralized robot management. Robot deployment and setup, logging, registering robot machines, dividing robots into groups to be managed separately, ability to attach an RDP user to a robot. 
3. Adding projects. Loading RPA projects created in Studio to be subsequently executed by a robot/robots. It is possible to attach to a project robots of specific versions.
4. Automation of RPA projects launch by using tasks. Using triggers to manage task launches. A trigger can be, for example, a schedule based on the organization workday calendar.
5. Strategies for assigning robots to RPA project execution. It allows defining the order in which robots will be assigned to a task, when the project is launched automatically.  
6. Manual launching of robots with RPA projects. You can select a deployed robot and manually launch project execution.
7. Working with data exchange queues. Queues are used to organize data exchange between robots, as well as between robots and Studio when executing RPA projects. 
8. Multi-tenancy. This is the ability to create tenants - “branches” of the organization for isolated access to system entities. Within the framework of a tenant, you can manage robot machines and tenant users.
9. User management. Setting up user accounts and assigning user roles to differentiate access rights. Integration with Active Directory is available - that way it is possible to use AD accounts instead of creating users within the system. 
10. Monitoring. There are 3 event journals: for Orchestrator, for the robots and for the projects. Journals can be accessed through the Orchestrator UI. For journal analytics the system provides access to the external Grafana system - it is not a part of Orchestrator and is provided as an add-on.

### Primo RPA Idea Hub

Primo RPA Idea Hub is a software product for comprehensive management of the robotization process. It has built-in tools for collection and analysis of suggestions for process automation within an organization, efficiency evaluation and monitoring of implementation status.

Key features:  
1. Facilitating interaction between robotization process participants and stakeholders.  
2. Integration with Primo platform, which ensures collection of data from other software of the product line for planning and analysis.  
3. Hosted or on-premise integration with customer infrastructure.  
4. Customizable role-based access model that supports AD and SSO.  
5. Flexible UI that can be customized in accordance with customer requirements and metrics.  
6. Visual representation of robotization results.  
7. Import and export from/to other products and IT systems. 


## System requirements

### Studio

To install and work with Primo Studio, user workstation has to meet the following requirements: 

| Hardware   |  Software  |
| ------------ | ------------- |
| CPU 4 core, RAM 8 Gb, HDD 100 Gb | <p>Microsoft Windows 7 (SP2) or up. </p> <p>Microsoft .NET Framework 4.6.1; Microsoft Visual C++ Runtime 14; Windows PowerShell.</p> <p>Local administrator rights (depending on the components used)</p> |

### Robot machine

To install and work with Primo Robot (both working with Orchestrator and as a stand-alone), Robot machine has to meet the following requirements:

| Hardware     |  Software | 
| ------------- | ------------- | 
| CPU 8 core, RAM 8 Gb, HDD 250 Gb  | Windows 10 / Windows Server 2016 and up | 
| CPU 6 core, RAM 8 Gb, HDD 250 Gb  | Linux: CentOS 8+, Ubuntu 20+, Astra Linux 1.7+ | 


### Orchestrator

To install and work with Primo Orchestrator, the server has to meet the following requirements:

| Server components   | Hardware  | Software  |
| ------------- | ------------- | ----- |
| Orchestrator server | CPU 8 core, RAM 16 Gb, HDD 200 Gb | Windows Server 2016 and up <p>Linux: CentOS 8+, Ubuntu 20+, Astra Linux 1.7+ </p> |
| DB server | CPU 8 core, RAM 16 Gb, HDD 200 Gb  | see above |
| Journal server | CPU 8 core, RAM 16 Gb, HDD 1000 Gb | see above |

### Idea Hub

To install and work with Primo Idea Hub, there are the following minimum and recommended requirements:

Minimum:

| Hardware    |  Software  |
| ------------ | ------------- |
| CPU 2 core, 2GHz, RAM 4 Gb, HDD 50 Gb | <p>Ubuntu 22.04 64 bit, CentOS 8 64 bit or similar;</p> <p>Windows Server 2016, 2019</p> |

Recommended:

| Hardware    |  Software  |
| ------------ | ------------- |
| CPU 4 core, 4GHz, RAM 8 Gb, HDD 200 Gb | <p>Ubuntu 22.04 64 bit, CentOS 8 64 bit or similar;</p> <p>Windows Server 2016, 2019</p> |

