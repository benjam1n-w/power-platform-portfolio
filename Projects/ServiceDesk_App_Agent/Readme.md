# Service Desk Application + Agent

 

## Problem

 

IT support teams often rely on manual ticket intake processes where users must fill out structured forms to report issues. This approach can be slow, inconsistent, and dependent on users correctly categorizing and prioritizing their requests.

 

---

 

## Goal

 

Build an intelligent service desk system that allows users to create support tickets either through a structured application or using natural language, while ensuring consistent categorization and prioritization.

 

---

 

## Solution

 

I built an end-to-end service desk solution using Microsoft Power Platform that combines:

 

- A **Power Apps interface** for structured ticket submission and management

- A **Copilot Studio agent** for natural language ticket creation

- A **Power Automate workflow** to process and create tickets in Dataverse

 

The system allows users to:

- Submit tickets manually via a form

- View and filter their existing tickets

- Create tickets through an AI agent using conversational input

 

---

 

## Key Features

 

- 🧾 Ticket creation via **Power App form**

- 🤖 Ticket creation via **AI agent (natural language)**

- 📊 Ticket dashboard with filtering (Status, Priority, Category)

- 🆔 Auto-assigned Ticket IDs

- ⚙️ Backend automation with Power Automate

- 🗄️ Centralized data storage in Dataverse

 

---

 

### 1. Home Screen

Entry point with navigation options:

- New Ticket

- My Tickets

- Policies

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/homescreen.png)

---

 

### 2. New Ticket Screen

Users can submit a ticket via a structured form including:

- Title

- Description

- Category

- Priority

 

Status is automatically assigned as: New

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/newticket.png)

---

 

### 3. My Tickets Screen

Displays user-specific tickets with:

- Ticket ID

- Priority

- Status

 

Includes filtering options:

- Status (dropdown)

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/mytickets.png)
 

---

 

## AI Agent Functionality

 

The Copilot agent enables ticket creation using natural language.

 

### Example:

 
![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/agent.png)

 

The agent:

- extracts relevant information 

- asks follow-up questions if needed 

- calls a Power Automate flow 

- creates tickets automatically

 

 

---

 

## Workflow (Power Automate)

 

The flow:

 

1. Receives data from the agent

2. Maps text inputs to Dataverse **Choice fields**

3. Creates a new ticket record

4. Returns a confirmation message to the user


![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/flow.png)

New record added to the application:

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/newticket_app.png)


---

 

## Data Model (Dataverse)

 

| Field        | Type                  |

|-------------|----------------------|

| Title       | Text (Primary column)|

| Description | Text                 |

| Category    | Choice               |

| Priority    | Choice               |

| Status      | Choice               |

| TicketID    | Text                 |


![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/Service_Desk_App_Agent/docs/dataverse.png)


---

 

## Design Decisions

 

- **Choice columns** used for Category, Priority, and Status to enforce consistency 

- **Status hidden from users** and assigned automatically 

- **Agent used as alternative input method**, not a replacement for forms 

- **Mapping logic implemented in flow** to handle Dataverse choice values 

- **Dropdown filters added** for usability in the ticket dashboard 

 

---

 

## Impact

 

This solution demonstrates:

 

- Integration of **AI agents with business applications**

- Handling of both **structured and unstructured input**

- Automation of ticket creation and classification

- Improved user experience through flexible input methods

 

---

 

## Tech Stack

 

| Component        | Technology                     |

|----------------|-------------------------------|

| Application UI | Power Apps (Canvas)           |

| Automation     | Power Automate                |

| AI Agent       | Copilot Studio                |

| Data Storage   | Dataverse                     |

| Data Logic     | Choice columns + mapping      |

| Integration    | Agent → Flow → Dataverse      |
