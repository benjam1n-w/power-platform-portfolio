# Smart E-mail Routing System

# Problem
Candidate profiles are received via email and must be sent manually to the correct hiring manager. This slowed down the process and created room for errors or missed profiles.

# Goal

Automate the routing of candidate emails so that each profile is instantly forwarded to the correct hiring manager.

# Solution

A Power Automate flow that triggers on incoming emails, extracts the Competency and Role from the subject line, matches them to active demands in an Excel file, and automatically forwards the candidate email to the assigned manager.

# Design Decisions

- Use the standardized email subject format:
Competency | Role | Name | Rate | Availability | Vendor
- Extract only the first two components (Competency + Role), which uniquely identify the demand.
- Reconstruct a CompetencyRole key matching the Excel table structure.
- Filter Excel rows only with Open or Pending approval/creation status to avoid routing to inactive roles.
- Forward the email using the ManagerEmail column from the matched row.

# Tools Used

Power Automate (trigger, parsing, filtering, forwarding)
Excel Online (Business) (demand tracker and manager mapping)

# Impact

Eliminated manual email routing in the recruitment process
Reduced errors and inconsistencies
Ensured candidate profiles reach the correct manager immediately
Improved overall speed and reliability of candidate handling

## Workflow Overview

### Screenshot of the Flow
![Flow Overview](screenshots/email_routing_flow.png)


