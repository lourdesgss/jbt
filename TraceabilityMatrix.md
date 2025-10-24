# Requirements/Use Cases Traceability Matrix

## Functional Requirements Traceability

| **Functional Requirements**       | UC-01 | UC-02 | UC-15 | UC-16 | UC-17 | UC-18 |
|-----------------------------------|-------|-------|-------|-------|-------|-------|
| FR-1 QR Code Access               | X     |       |       |       |       |       |
| FR-2 Language Selection           | X     |       |       |       |       |       |
| FR-3 Safety Information Display   | X     |       |       |       |       |       |
| FR-4 Visitor Form Completion      | X     |       |       |       |       |       |
| FR-5 Form Submission              | X     |       |       |       |       |       |
| FR-6 Visitor Response             | X     | X     | X     |       |       |       |
| FR-7 Bypass Form Option           | X     |       |       |       |       |       |
| FR-8 Operator Portal Access       | X     | X     |       |       |       |       |
| FR-9 Instant Request Notification | X     | X     |       |       |       |       |
| FR-10 Request Information Display | X     | X     |       |       |       |       |
| FR-11 Form Translation            | X     | X     |       |       |       |       |
| FR-12 Approve/Deny Requests       | X     | X     |       |       |       |       |
| FR-13 Request History             |       | X     |       |       |       |       |
| FR-14 Video Feedback              |       | X     |       |       | X     |       |
| FR-15 Request Queue               |       | X     |       |       |       |       |
| FR-16 Intercom Status             |       |       |       |       |       | X     |
| FR-17 Gate Operation Logging      | X     | X     | X     | X     |       |       |
| FR-18 Log Download and Search     |       |       |       | X     |       |       |

## User Story Traceability

| **User Stories**                       | UC-01 | UC-02 | UC-15 | UC-16 | UC-17 | UC-18 |
|----------------------------------------|-------|-------|-------|-------|-------|-------|
| US-01 QR Code Scan                     | X     |       |       |       |       |       |
| US-02 Set Application Language         | X     |       |       |       |       |       |
| US-03 Get Security Information         | X     |       |       |       |       |       |
| US-04 Choose to Bypass Form            | X     |       |       |       |       |       |
| US-05 Fill in Entrance Form            | X     |       |       |       |       |       |
| US-06 Receive Response with Info       | X     | X     |       |       |       |       |
| US-07 Redirection to Correct Address   | X     | X     |       |       |       |       |
| US-08 Notification of Incoming Visitor |       | X     |       |       |       |       |
| US-09 Receive Translated Form          |       | X     |       |       |       |       |
| US-10 Approve/Deny Form                |       | X     |       |       |       |       |
| US-11 Open Gate                        |       | X     |       |       |       |       |
| US-12 Access Gate Logs                 |       |       | X     |       |       |       |
| US-13 Obtain Data for Analysis         |       |       |       | X     |       |       |


## 3-way Matrix

### Traceability Matrix: Functional Requirements, Use Cases, and User Stories

| **Functional Requirement**        | **Associated Use Cases**   | **Associated User Stories** | **Description / Notes**                                                            |
|-----------------------------------|----------------------------|-----------------------------|------------------------------------------------------------------------------------|
| FR-1 QR Code Access               | UC-01                      | US-01                       | Enables visitors to scan a QR code to initiate the access process.                 |
| FR-2 Language Selection           | UC-01                      | US-02                       | Allows visitors to select a preferred language for interaction.                    |
| FR-3 Safety Information Display   | UC-01                      | US-03                       | Displays security or safety information to visitors before form entry.             |
| FR-4 Visitor Form Completion      | UC-01                      | US-05                       | Provides a digital form for visitors to complete required details.                 |
| FR-5 Form Submission              | UC-01                      | US-06                       | Submits visitor form data to the system for operator review.                       |
| FR-6 Visitor Response             | UC-01, UC-02, UC-15        | US-06, US-07                | Delivers response or redirection to visitors after submission.                     |
| FR-7 Bypass Form Option           | UC-01                      | US-04                       | Allows visitors to skip form completion under certain conditions.                  |
| FR-8 Operator Portal Access       | UC-01, UC-02               | US-08, US-10, US-11         | Provides operators with portal access for reviewing and managing visitor requests. |
| FR-9 Instant Request Notification | UC-01, UC-02               | US-08                       | Sends instant notifications to operators upon visitor form submission.             |
| FR-10 Request Information Display | UC-01, UC-02               | US-09                       | Displays visitor request information for operator review.                          |
| FR-11 Form Translation            | UC-01, UC-02               | US-09                       | Translates submitted form data into the operator’s preferred language.             |
| FR-12 Approve/Deny Requests       | UC-01, UC-02               | US-10                       | Enables operators to approve or deny incoming visitor requests.                    |
| FR-13 Request History             | UC-02                      | US-12                       | Allows operators to view historical visitor request data.                          |
| FR-14 Video Feedback              | UC-02, UC-17               | US-11                       | Enables visual feedback (video intercom) between visitor and operator.             |
| FR-15 Request Queue               | UC-02                      | US-08                       | Displays a queue of pending requests for the operator.                             |
| FR-16 Intercom Status             | UC-18                      | US-11                       | Monitors and displays the live intercom connection status.                         |
| FR-17 Gate Operation Logging      | UC-01, UC-02, UC-15, UC-16 | US-12                       | Records all gate operation actions for auditability.                               |
| FR-18 Log Download and Search     | UC-16                      | US-13                       | Enables operators to download and search gate logs for analysis.                   |
