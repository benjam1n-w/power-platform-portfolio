# AI Invoice Processing Agent

## Problem

Invoice processing often requires manual data entry, validation, and approval routing. This process is time-consuming, error-prone, and lacks standardization, especially for high-value invoices requiring managerial approval.

---

## Goal

Automate invoice intake, validation, storage, and approval workflows using natural language input, reducing manual effort and improving data consistency.

---

## Solution

I built a Copilot Studio agent integrated with Power Automate that:

- Accepts invoice data through natural language interaction
- Extracts structured fields (vendor, invoice number, amount, date)
- Validates input and prompts for missing information
- Stores invoice records in Dataverse
- Automatically approves low-value invoices
- Routes high-value invoices through an approval workflow
- Updates the invoice status based on approval outcome

---

## Design Decisions

The solution was designed to separate responsibilities between the agent and backend workflow.

The Copilot agent handles:
- natural language understanding
- data collection and validation
- user interaction and confirmation

Power Automate handles:
- business logic execution
- data processing and storage
- approval orchestration

InvoiceNumber was designed as a text field to reflect real-world formats (e.g. INV-123), avoiding issues with numeric constraints.

Explicit mapping instructions were added to improve reliability of AI-driven field extraction and prevent incorrect parameter assignment.

The approval logic was set with a configurable threshold to simulate real governance rules for high-value transactions.

---

## Tools Used

- Microsoft Copilot Studio  
- Power Automate  
- Microsoft Dataverse  
- Outlook / Power Automate Approvals  

---

## Impact

This solution demonstrates how AI and automation can be combined to streamline business processes.

It reduces manual data entry, enforces structured validation, and introduces automated approval workflows for high-value transactions.

The design reflects a realistic enterprise scenario, showcasing how conversational AI can act as a front layer for structured backend automation.

---

## Status

- Fully functional  
- End-to-end workflow implemented  
- Integrated AI + automation solution  
- Ready for demonstration and portfolio use  
