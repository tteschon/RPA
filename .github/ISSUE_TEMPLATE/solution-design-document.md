---
name: Solution Design Document
about: Solution Design Document Template
title: Solution Design Document
labels: documentation
assignees: ''

---

# [Automation Name]

## Short Description of the process
[Short Description goes here].

*This project uses the UIPath Performer process model which is used to pull transaction items from an orchestrator queue and process them as needed.*

## Master Project Details
Item | Details
--- | ---
Master Project Name & Version | [Automation Name] 1.0
Robot Type <br> *(Attenended/Unattended/Mixed)* | Unattended
Is Orchestrator used? *(Yes/No)* | Yes
Scalable? <br> *(Can process be run by multiple bots in parallel?)* | Yes - multiple performers can be used with a single queue.

## Runtime Guide
### List of Packages
Package Name | High-Level Description
--- | ---
[UIPath System Activities](https://docs.uipath.com/activities/docs/about-the-system-activities-pack) | Core activities which enable the robots to manipulate data tables and collections, work with files and folders, communicate with Orchestrator. Package also contains workflow operators, dialog forms, debugging and invoking methods.
[UIPath Mail Activities](https://docs.uipath.com/activities/docs/about-the-mail-activities-pack) | Retrieve and send mail using POP3, IMAP, SMTP and Exchange protocols.
[UIPath Excel Activities](https://docs.uipath.com/activities/docs/about-the-excel-activities-pack) | Execute Excel related operations using the Open Office XML format (XLSX) or Excel.Interop
[UIPath UIAutomation Activities](https://docs.uipath.com/activities/docs/about-the-ui-automation-activities-pack) | Package contains core activities which enable the automation of desktop applications, browsers, and virtual machines.
### Master Project Runtime Details
Item | Details
--- | ---
Production Environment Details | 
Prerequisites to run |
Input Data |
Expected Output (output data) | 
How to start the automated process? |
Resuming the process from a particular step | 
Reporting <br> *(queues reporting, Kibana or another platform)* | 
Manual Error Handling <br> *Roll back or manually complete failed transactions. <br> Procedures to reset the item. (Eg. “set status as investigating")*| 
How to resume the process in case of error | 
How to manually fix transactions with error | 
Password Policies <br> *Specific compliance requests?* |
Stored Credentials <br> *Never hard code credentials in the workflow* | 
List of Asset Names |
List of Queues Name |
Schedule Details |

### **Applications**
---
App & Version | Client Type | Environment | Location
--- | --- | --- | ---
[App 1] | Thin | Dev | Link
[App 1] | Thick | Prod | Link

### **Project Details**
This section describes all the projects that compose the automated process. 
For each project, the workflow(s) are described in the logical order that they are called in.<br>

## Project: Performer
Item | Details
--- | ---
Environment used for development <br> *Name, location, configuration details etc* | 
Environment prerequisites <br> *OS details, libraries, required apps* | 
Logging level | 
Details about automation <br> *if the apps were automated using UI Automation, Image & Text* |
In case of attended bot, can the user operate the computer while the robot is running? |
Repository for project <br> *where the developed project is stored* | Github
List of reused components | 
Custom logs defined in the workflows <br> *where Throw Activity was used or custom log message was defined* | 
Frequent errors found in the development phase | 
Workarounds used in the automation phase | 
Configuration method <br> *assets, excel file, Json file* | 
Configuration details <br> *path for input files, configuration Orchestrator assets used* | 

### Workflow(s) specific to the Project 
*All the workflow files (.xaml files) used in the project, with the Input and Output data.*

| Workflow File Name | Description | Pre-Condition | Post-Action | Agruments | Comments |
| --- | --- | --- | --- | --- | --- |
| *Process.xaml*| *This is the workflow description* | *This is the workflow pre-condition* | *This is the workflow Post-Action* | *Workflow Arugment 1* | *Workflow Comment* |

## **Glossary**

- **Activity** - an action that the robot executes.
- **Assets** - Shared variables or configurations that are invoked in the design processes by developers and used in processes.
- **Dispatcher/Producer** - Automation solution that creates and pushes transaction items to an Orchestrator queue.
- **Flowchart** - a workflow where activities are connected by arrows and the logic of the workflow can be easily followed in a visual manner. The flowchart can also be exported as an image from UiPath studio.
- **Job** - is the execution of a process on one or multiple Robots.
- **Library** - is a package which contains multiple reusable components.
- **Master project** - the overall output of the development, containing one or multiple projects that together cover the scope of the robotic process automation.
- **Orchestrator** – Enterprise architecture server platform supporting: release management, centralized logging, reporting, auditing and monitoring tools, remote control, centralized scheduling, queue/robot workload management, assets management.
- **Package** - the output of compiling a project. A package can be deployed on the robot machine and be executed by the robot service. Only one package can be executed at a given time by a robot. The package is used when defining the running phase of the automation
- **Performer/Consumer** - Automation solution that pulls transaction items from an Orchestrator queue and processes them.
- **Project** - a UiPath Studio project containing one or multiple workflow files. A project can be converted to a package and run independently, covering a particular scope within the master project. The project is used when defining the development and support phase of the automation.
- **Sequence** - a workflow where activities are executed one after another, in a sequential order.
- **State machine** - a more advanced way of organizing a workflow, similar to a flowchart.
- **Storage Buckets** - are used to provide a per-folder storage solution for RPA developers to leverage in creating automation projects.
- **Triggers** - enable you to execute jobs in a preplanned manner, at regular intervals (time triggers) or whenever new items are added to your queues (queue triggers).
- **Workflow** - a component of the package, the workflow encapsulates a part of the project logic. The workflow can be of type: sequence, flowchart or state machine. a workflow is saved as an .xaml file inside the project folder. A workflow file can be invoked from another workflow and by default there is an initial workflow file that will run when executing the package.
