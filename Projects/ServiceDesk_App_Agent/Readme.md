# Service Desk Application + AI Agent

## Problem

IT support teams often rely on manual ticket intake processes where users must fill out structured forms to report issues. This approach is time-consuming, inconsistent, and depends on users correctly categorizing and prioritizing their requests.

---

## Goal

Build an intelligent service desk system that enables users to create support tickets either through a structured application or via natural language, while maintaining consistent categorization and prioritization.

---

## Solution

An end-to-end service desk solution built using Microsoft Power Platform, combining:

- **Power Apps (Canvas)** for ticket creation and management
- **Copilot Studio** for natural language interaction
- **Power Automate** for backend processing
- **Dataverse** for structured data storage

The system allows users to:

- Submit tickets via a structured form
- View and filter their tickets
- Create tickets using conversational AI

---

## Tech Stack

| Component | Technology |
|----------------|---------------------------|
| Application UI | Power Apps (Canvas) |
| Automation | Power Automate |
| AI Agent | Copilot Studio |
| Data Storage | Dataverse |
| Data Logic | Choice columns + mapping |
| Integration | Agent → Flow → Dataverse |

---

## Key Features

- 🧾 Ticket creation via **Power Apps form**
- 🤖 Ticket creation via **AI agent (natural language)**
- 🔍 Full-text search across multiple ticket fields
- 🎛️ Advanced filtering (Status, Priority, Category)
- 📊 Table-style ticket dashboard
- 🆔 Ticket ID tracking
- 💬 Controlled comment system
- 🗑️ Safe deletion with confirmation popup
- ⚙️ Automated backend processing
- 🗄️ Structured data storage in Dataverse

---

## Application Screens

### 1. Home Screen

Navigation hub with:

- New Ticket
- My Tickets
- Policies

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/homescreen.jpg)

---

### 2. New Ticket Screen

Structured ticket submission form:

- Title
- Description
- Category
- Priority

Status is assigned automatically: New

Additional UX:

- Confirmation notification after submission
- Contextual navigation to "My Tickets"

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/newticket.jpg)

---

### 3. My Tickets Screen

Structured table-style view displaying:

- Title
- Ticket ID
- Priority
- Status

Features:

- Full-text search (Title, Description, ID, fields)
- Status-based filtering
- Combined filtering and search
- Visual column layout with headers and separators

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/mytickets.jpg)

---

### 4. Ticket Details Screen

Detailed view of a selected ticket:

- Full ticket information
- Read-only core fields
- Controlled interaction model
  
![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/ticket_details.jpg)


Includes:

- Add Comment functionality (on-demand input)
- Single-comment restriction per ticket
- Input validation and length limitation

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/addcomment.jpg)

- Deletion option with confirmation pop up

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/ticket_delete.jpg)


---

## AI Agent Functionality

The Copilot agent enables ticket creation through natural language.

### Example

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/agent.jpg)

The agent:

- extracts relevant data from user input
- asks follow-up questions when needed
- maps input into structured fields
- triggers ticket creation via Power Automate

---

## Workflow (Power Automate)

The flow performs:

1. Receives input from the agent
2. Maps text to Dataverse Choice values
3. Creates a new ticket record
4. Returns confirmation with Ticket ID

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/flow.jpg)

Created record:

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/ticketfromagent.jpg)

---

## Data Model (Dataverse)

| Field | Type |
|-------------|-----------------------|
| Title | Text (Primary column) |
| Description | Text |
| Category | Choice |
| Priority | Choice |
| Status | Choice |
| TicketID | Text |

![](https://raw.githubusercontent.com/benjam1n-w/power-platform-portfolio/main/Projects/ServiceDesk_App_Agent/docs/data.jpg)

---

## Design Decisions

- Use of **Choice columns** for standardized classification
- **Status controlled by system**, not user-editable
- **Limited editing model** to ensure data integrity
- **Comment-based interaction** instead of full record editing
- **Table-style UI layout** for better readability
- **Search + filter combination** for efficient navigation
- **Confirmation-based deletion** to prevent data loss

---

## Impact

This solution demonstrates:

- Integration of **AI with business applications**
- Handling of both **structured and unstructured input**
- Transition from form-based systems to **intelligent workflows**
- Strong focus on **UX, data integrity, and real-world constraints**  
