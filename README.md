# Detailed Security Risk Analysis and Requirements

# Table of Contents
1. [Executive Summary](#executive-summary)
2. [Introduction](#introduction)
   1. [Purpose](#purpose)
   2. [Scope of this Risk Assessment](#scope-of-this-risk-assessment)
3. [Risk Assessment Approach](#risk-assessment-approach)
   1. [Participants](#participants)
   2. [Techniques Used](#techniques-used)
   3. [Risk Model](#risk-model)
4. [System Characterization](#system-characterization)
   1. [Technology Components – The Protection Lab Company (TPL)](#technology-components--the-protection-lab-company-tpl)
   2. [Physical Location(s)](#physical-locations)
   3. [Data Used by System](#data-used-by-system)
   4. [Users – Rank Based](#users--rank-based)
   5. [Flow Diagram – Risk Assessment Activities](#flow-diagram--risk-assessment-activities)
5. [Vulnerability Statement](#vulnerability-statement)
6. [Risk Assessment Results](#risk-assessment-results)

# Security Risk Analysis 2
## Executive Summary
Factors such as size, growth rate, resources, and asset portfolio affect the depth of risk assessment models. Organizations can carry out generalized assessments when experiencing budget or time constraints. However, generalized assessments don’t necessarily provide detailed mappings between assets, associated threats, identified risks, impact, and mitigating controls. To highlight high-risk findings, there are six simple steps in the risk management process: identify your risks; analyze the risks; control the risks; monitor those risks; improve your risk management, and report progress.

# Security Risk Analysis 3
## DETAILED ASSESSMENT
### 1. Introduction
#### 1.1 Purpose
IT enterprise security risk assessments are performed to allow organizations to assess, identify and modify their overall security posture and to enable security, operations, organizational management, and other personnel to collaborate and view the entire organization from an attacker's perspective.
#### 1.2 Scope of this Risk Assessment
The scope of risk assessment identifies the various information assets that could be affected by a cyber attack (such as hardware, systems, laptops, customer data, and intellectual property), and then identifies the various risks that could affect those assets. Also, a risk assessment is intended to estimate potential human health and environmental risks posed by current and potential future conditions assuming no further remediation of the Facility.

### 2. Risk Assessment Approach
#### 2.1 Participants
**Role | Participant**
System Owner | The Protection Lab
System Custodian | The Protection Lab
Security Administrator | Josue Martinez Arias
Database Administrator | Fatima Shahram
Network Administrator | Jose-Luis Ortiz
Risk Assessment Administrator | Mason Ung

#### 2.2 Techniques Used
**Technique | Description**
Risk Assessment | Assessing risk from Tiers: 1. the Organization 2. Mission/ Business 3. Information Systems
Risk Assessment Process | The four steps for assessing risk: 1. Prepare for Assessment 2. Conduct Assessment 3. Communicate Results 4. Maintain Assessment

#### 2.3 Risk Model
The Risk Model defines the risk factors to be assessed and the relationship among those factors. Risk factors are characteristics used in risk models as inputs to determine levels of risk in risk assessments.
- Threats
- Vulnerabilities and Predisposing Conditions
- Likelihood
- Impact

### 3. System Characterization
System characterization is the process of defining the information assets that require a risk analysis. Information assets that require protection – that includes infrastructure, workflows, key assets, and resources. System characterization requires an inventory of major applications and general support systems. The following are some examples of major applications and their probable owners:
- Syxsense
- Netsparker
- Wireshark

General support systems are the systems used throughout the organization to support one or more. The following are some examples of general support systems:
- Laptops, tablets, smartphones, and other mobile devices
- Computer workstations
- Network (wired and wireless)

In assessing risks for an IT system, the first step is to define the scope of the effort. In this step, the components of the IT system are identified, along with the resources and the information that constitute the system. Characterizing an IT system establishes the scope of the risk assessment effort, defines the operational authorization, and provides information like hardware, software, system connectivity, and responsible division or support personnel –essential to defining the risk.

#### 3.1 Technology components – The Protection Lab Company (TPL)
**Component | Description**
IT System | Description and Components TPL is a distributed client-server application transported by a network provided by ABC, a third party. Here are some of the major components:
- A Sparc SUNW, Ultra Enterprise 3500 server running SunOS 5.7 (Solaris 7). The server has four (4) processors running at 248 MHz, 2048 of memory, 4 SBus cards, 4 PCI cards, and total disk storage capacity of 368.6 GB
- One network interface that is connected to TPL data center Cisco switch. This interface is assigned two unique IP addresses.
- An Oracle 9i data store with two (2) commercial off-the-shelf (COTS) application modules (ABC and XYZ) purchased from Oracle Corporation

**IT System Interfaces and Protocols**
- An interface between TPL and the Budget Consolidation System (TPL). This interface allows only the BCS to securely transit data using the Secure Copy Protocol (SCP) on port 22 into the TPL.
- A modem for emergency dial-in support and diagnostics, secured via the use of a one-time password authentication mechanism.

#### 3.2 Physical Location(s)
**Location | Description**
TPL Data Center | 342 Elm Street, San Diego, California

#### 3.3 Data Used by System
**Data | Description**
Data Elements | Client software located within the Agency’s Windows 2003 Server Active Directory Domain to manage access to TPL. This software utilizes encrypted communications between the client and the server and connects to the server on port 1521. Only users with the appropriate rights within the BFA Domain can access the client software, although a separate client login and password is required to gain access to TPL data functions.

#### 3.4 Users – Rank Based
**Rank Based on Risk | Description**
Number of Users | Starting with the application with the greatest number of users
Type of Information | The more sensitive the information, the higher the risk i.e., bank account numbers, social security numbers
Use of the Information | Determine whether it’s research, business intelligence
Availability of Information | Hosted in the cloud, standalone system
Mobility of the Information | The more mobile, the greater the risk

#### 3.5 Flow Diagram – Risk Assessment Activities

### 4. Vulnerability Statement
**Vulnerability | Description**
V-220706 | High Windows 10 systems must be maintained at a supported servicing level.
V-220707 | High Administrative accounts must not be used with applications that access the Internet, such as web browsers, or with potential Internet sources, such as email.
V-220812 | High Credential Guard must be running on Windows 10 domain-joined systems.
V-220829 | High Autoplay must be disabled for all drives.
V-220857 | High The Windows Installer Always install with elevated privileges must be disabled.

### 5. Risk Assessment Results
**Item Number | Observation | Threat-Source/Vulnerability | Existing Controls | Likelihood | Impact | Risk Rating | Recommended Controls**
001 | User system passwords can be guessed or cracked | Previous employee | Password Policy | High | High | High | Reevaluate Password Policy
002 | Burglar break-in, past employee | Faulty physical security | Fences, Cameras | Low | High | High | Implement automated methods like picture IDs, biometrics
003 | Natural Disasters-Earth Quake | Broken pipe can cause flooding in the server room | Cold site | Low | High | Low | UPS, redundant ISP
004 | Accidental human interference – Accidental disclosure of information | Employee being duped into releasing sensitive information, sending data to wrong email address | Backups are taken regularly | Medium | High | Medium | Continue monitoring permissions changes, privileged users and backups.
