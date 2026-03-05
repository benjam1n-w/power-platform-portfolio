
# Project 2 — Vendor Demand Submission Power App

## Overview
A Canvas Power App built to streamline vendor demand submissions. The app writes to
SharePoint, triggers a Power Automate flow, and handles structured vendor data
selection using ComboBox controls with multi-select capability.

Although enterprise DLP restrictions prevented automated external emailing,
the app functions fully for internal use and demonstrates complex Power Apps +
Power Automate integration.

## Features
- Canvas App using collections, ComboBox multi-select, and structured data.
- Writes demands to SharePoint lists.
- Calls a Power Automate flow via PowerAppV2 connector.
- Multi-vendor selection passed as an array to Flow.
- JSON parsing and data transformation in Flow.
- Error handling and validation logic in both App + Flow.

## Technical Components
- Power Apps (.msapp source file included)
- Power Automate flow (export + screenshots)
- SharePoint list schema
- App architecture diagram

## Files Included
- `artifacts/VendorDemandApp.msapp` — Full source of the Canvas App
- `flows/VendorNotificationFlow.json` — Exported Flow definition
- `schema-diagram.png` — Data structure diagram
- `flow-overview.png` — Flow steps overview
- Screenshots of core app screens

## Skills Demonstrated
- Canvas App development (Power Fx, UI design)
- Power Automate integration
- SharePoint list modeling
- Business process automation
- Error handling and data validation
