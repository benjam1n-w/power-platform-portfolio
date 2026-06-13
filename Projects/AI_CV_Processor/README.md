# AI CV Processor

## Problem

Recruitment teams often need to manually review CVs and extract key candidate information into structured systems. This process is time-consuming, repetitive, and prone to inconsistencies, especially when dealing with high volumes of incoming applications.

---

## Goal

Automate the extraction of structured candidate data from CV documents using AI, and store the results in a centralized data store for further processing.

---

## Solution

I built an AI-powered pipeline using Microsoft Power Platform that:

- Monitors incoming emails with CV attachments
- Uses AI Builder to extract structured data from CV documents
- Processes extracted information automatically
- Stores candidate data in Dataverse for further use

The solution eliminates manual CV review and enables scalable candidate processing.

---

## Design Decisions

The solution uses a custom AI Builder document processing model trained on multiple CV formats to handle unstructured input.

A limited set of high-value fields was selected to optimize model accuracy:
- Full Name
- Email
- Skills
- Experience

The system processes email attachments dynamically using Power Automate to simulate a real-world intake pipeline.

The Experience and Skills fields were configured as multi-line text in Dataverse to handle long extracted content.

PNG format was used for training data to improve extraction consistency and avoid common PDF parsing issues.

---

## Workflow Overview

### 1. Email Trigger
Incoming emails with CV attachments trigger the flow automatically.

./docs/screen_1.png

---

### 2. AI Extraction
AI Builder processes the CV and extracts structured candidate data.

./docs/screen_2.png

---

### 3. Data Storage
Extracted data is stored in Dataverse for further processing and analysis.

./docs/screen_3.png

---

## Data Model (Dataverse)

| Field       | Type                  |
|------------|-----------------------|
| FullName   | Single line of text   |
| Email      | Single line of text   |
| Skills     | Multiple lines of text|
| Experience | Multiple lines of text|

---

## Tech Stack

| Component              | Technology                          |
|------------------------|-------------------------------------|
| AI processing          | AI Builder (Custom Document Model)  |
| Automation             | Power Automate                      |
| Data storage           | Microsoft Dataverse                 |
| Input source           | Outlook Email (V3 trigger)          |
| Data format            | PNG images (CVs)                    |
| Platform               | Power Platform                      |

---

## Impact

This solution demonstrates how AI can be used to automate unstructured data processing in recruitment workflows.

It removes the need for manual data extraction from CVs, improves consistency, and enables scalable candidate intake.

The project highlights the integration of AI Builder with automation tools to create intelligent business processes.

---

## Status

- Fully functional  
- AI model trained and integrated  
- End-to-end automation implemented  
- Ready for portfolio demonstration  
