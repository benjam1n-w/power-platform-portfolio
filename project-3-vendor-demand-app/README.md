
# Project 3 — Vendor Demand Submission Power App (Concept Documentation)

## Overview
This project is a Power Apps + Power Automate solution designed to streamline
the process of submitting vendor demands inside a corporate environment.

The app allows users to:
- Select one or many vendors
- Fill in a structured demand form
- Submit to SharePoint
- Trigger a Power Automate flow that processes the submission

Due to enterprise DLP policies, automated external emailing was restricted.
The architecture was adapted to remain compliant while keeping a smooth user
workflow.

## My Role
- Designed the Canvas App UI/UX
- Built Power Fx logic for validation, collections, and data structuring
- Built an internal Power Automate flow triggered via PowerAppV2
- Integrated with SharePoint for data storage
- Implemented JSON parsing and vendor processing logic

## Skills Demonstrated
- Canvas App development (Power Fx)
- Power Automate orchestration
- SharePoint data modeling
- Working with multi-select ComboBoxes
- Transforming data for flows
- Handling DLP / enterprise constraints
- Building scalable internal process automation


## Problems This App Solved

Before this solution, demand requests had to be emailed manually to up to **15 vendors**
for every case. This caused several operational issues:

- **High risk of human error** — requesters copied details manually for every vendor,
  which often led to mistakes or missing information.
- **Inconsistent communication** — each requester wrote emails differently, and
  important fields were sometimes forgotten.
- **Time‑consuming workflow** — sending many separate emails for every demand took
  several minutes per case.
- **No standardization** — vendors received slightly different versions of the same
  message depending on who sent it.

The Power App centralizes and standardizes the entire submission workflow. All required
details are entered once, the vendor list is validated inside the app, and the data is
submitted in a structured way to SharePoint. This results in a process that is:

- **faster**
- **consistent**
- **standardized**
- **far less error‑prone**

Even though external emails must still be confirmed manually due to DLP restrictions,
the application eliminates the repetitive manual work and removes the root causes of
most errors.

## Architecture Summary (High-Level)
User → Power App → SharePoint → Power Automate → Internal Processing

## Notes
All app assets and screenshots are excluded from this repository as they are part
of a restricted enterprise tenant. This folder contains only conceptual
documentation.
