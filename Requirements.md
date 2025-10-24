# System Requirements

## Functional Requirements

1. The system shall allow users to access the visitors portal by scanning a qr code [FR-1](#fr-1-qr-code-access)
2. The system shall allow users to choose their preferred language [FR-2](#fr-2-language-selection)
3. The system shall allow users to see the safety information necessary to go into the premises [FR-3](#fr-3-safety-information-display)
4. The system shall allow users to fill out the visitor's form with the information required [FR-4](#fr-4-visitor-form-completion)
5. The system shall allow users to submit the form [FR-5](#fr-5-form-submission)
6. The system shall allow users to receive a response with information (where to park, or if it's the incorrect address) [FR-6](#fr-6-visitor-response)
7. The system shall allow users to bypass the form filling process, if they so wish [FR-7](#fr-7-bypass-form-option)

8. The system shall allow users to access the operator's portal via a web app/mobile app [FR-8](#fr-8-operator-portal-access)
9. The system shall allow users to see incoming requests instantly, using a phone call-like notification [FR-9](#fr-9-instant-request-notification)
10. The system shall allow users to open the portal and see the request and its information [FR-10](#fr-10-request-informtion-display)
11. The system shall allow users to see the forms in Dutch, independently of the selected language in the visitor's portal [FR-11](#fr-11-form-translation)
12. The system shall allow users to either approve/deny the request or reply to the request with extra information [FR-12](#fr-12-approvedeny-requests)
13. The system shall allow users to see a history of recent requests [FR-13](#fr-13-request-history)
14. The system shall allow users to have video feedback of the gate through the API [FR-14](#fr-14-video-feedback)
15. The system shall allow incoming requests to be queued if the operator isn't available [FR-15](#fr-15-request-queue)
16. The system shall allow users to see the intercom's status (available, not available) [FR-16](#fr-16-intercom-status)

17. The system shall log all gate operations in a database [FR-17](#fr-17-gate-operation-logging)
18. The system shall allow users to download and search through logs [FR-18](#fr-18-log-download-and-search)

### FR-1: QR Code Access

| **ID**             | FR-1                                                     |
|--------------------|----------------------------------------------------------|
| **Name**           | QR Code Access                                           |
| **Input**          | Visitor scans QR code                                    |
| **Process**        | System validates QR code and redirects to visitor portal |
| **Output**         | Visitor redirected to portal                             |
| **Error Handling** | Show invalid QR code message                             |

### FR-2: Language Selection

| **ID**             | FR-2                                                  |
|--------------------|-------------------------------------------------------|
| **Name**           | Language Selection                                    |
| **Input**          | Visitor selects preferred language                    |
| **Process**        | System switches portal interface to selected language |
| **Output**         | Visitor sees portal in selected language              |
| **Error Handling** | Default to English or show error message              |

### FR-3: Safety Information Display

| **ID**             | FR-3                                               |
|--------------------|----------------------------------------------------|
| **Name**           | Safety Information Display                         |
| **Input**          | Visitor opens portal                               |
| **Process**        | System retrieves safety instructions from database |
| **Output**         | Display safety information to visitor              |
| **Error Handling** | Show “information unavailable” message             |

### FR-4: Visitor Form Completion

| **ID**             | FR-4                                   |
|--------------------|----------------------------------------|
| **Name**           | Visitor Form Completion                |
| **Input**          | Visitor fills out required form fields |
| **Process**        | System validates inputs                |
| **Output**         | Form ready to be submitted             |
| **Error Handling** | Highlight invalid or missing fields    |

### FR-5: Form Submission

| **ID**             | FR-5                                                   |
|--------------------|--------------------------------------------------------|
| **Name**           | Form Submission                                        |
| **Input**          | Visitor submits completed form                         |
| **Process**        | System stores form data and triggers response workflow |
| **Output**         | Visitor receives confirmation or next steps            |
| **Error Handling** | Show submission error message and allow retry          |

### FR-6: Visitor Response

| **ID**             | FR-6                                  |
|--------------------|---------------------------------------|
| **Name**           | Visitor Response                      |
| **Input**          | Submitted visitor form                |
| **Process**        | Operator checks data and replies      |
| **Output**         | Visitor receives appropriate response |
| **Error Handling** | Show “unable to process” message      |

### FR-7: Bypass Form Option

| **ID**             | FR-7                                                 |
|--------------------|------------------------------------------------------|
| **Name**           | Bypass Form Option                                   |
| **Input**          | Visitor chooses to bypass form                       |
| **Process**        | System skips form workflow and submits empty request |
| **Output**         | Visitor gains direct access to the facilities        |
| **Error Handling** | N/A                                                  |

### FR-8: Operator Portal Access

| **ID**             | FR-8                                |
|--------------------|-------------------------------------|
| **Name**           | Operator Portal Access              |
| **Input**          | Operator logs in via web/mobile app |
| **Process**        | System authenticates user           |
| **Output**         | Operator sees portal homepage       |
| **Error Handling** | Show login error message            |

### FR-9: Instant Request Notification

| **ID**             | FR-9                                         |
|--------------------|----------------------------------------------|
| **Name**           | Instant Request Notification                 |
| **Input**          | Incoming visitor request                     |
| **Process**        | System triggers phone call-like notification |
| **Output**         | Operator notified immediately                |
| **Error Handling** | Queue notification if device unreachable     |

### FR-10: Request Information Display

| **ID**             | FR-10                                  |
|--------------------|----------------------------------------|
| **Name**           | Request Information Display            |
| **Input**          | Operator opens request                 |
| **Process**        | System retrieves request details       |
| **Output**         | Operator sees request and visitor info |
| **Error Handling** | Show “request unavailable” message     |

### FR-11: Form Translation

| **ID**             | FR-11                                           |
|--------------------|-------------------------------------------------|
| **Name**           | Form Display in Dutch                           |
| **Input**          | Request data, visitor portal language selection |
| **Process**        | System converts or displays forms in Dutch      |
| **Output**         | Operator sees form in Dutch                     |
| **Error Handling** | Show “unable to load form” message              |

### FR-12: Approve/Deny Requests

| **ID**             | FR-12                                     |
|--------------------|-------------------------------------------|
| **Name**           | Approve/Deny Requests or Reply            |
| **Input**          | Operator chooses to approve/deny or reply |
| **Process**        | System processes decision or message      |
| **Output**         | Visitor receives decision or reply        |
| **Error Handling** | Show “unable to process request” message  |

### FR-13: Request History

| **ID**             | FR-13                                 |
|--------------------|---------------------------------------|
| **Name**           | Request History                       |
| **Input**          | Operator opens history view           |
| **Process**        | System retrieves recent requests      |
| **Output**         | Operator sees list of recent requests |
| **Error Handling** | Show “history unavailable” message    |

### FR-14: Video Feedback

| **ID**             | FR-14                            |
|--------------------|----------------------------------|
| **Name**           | Video Feedback                   |
| **Input**          | Operator requests gate video     |
| **Process**        | System fetches video via API     |
| **Output**         | Video displayed to operator      |
| **Error Handling** | Show “video unavailable” message |

### FR-15: Request Queue

| **ID**             | FR-15                                        |
|--------------------|----------------------------------------------|
| **Name**           | Request Queue                                |
| **Input**          | Incoming request, operator unavailable       |
| **Process**        | System queues request                        |
| **Output**         | Request processed when operator is available |
| **Error Handling** | Retain request until processed               |

### FR-16: Intercom Status

| **ID**             | FR-16                                      |
|--------------------|--------------------------------------------|
| **Name**           | Intercom Status                            |
| **Input**          | System monitors intercom                   |
| **Process**        | System checks availability                 |
| **Output**         | Status displayed (available/not available) |
| **Error Handling** | Show “status unknown” message              |

### FR-17: Gate Operation Logging

| **ID**             | FR-17                                  |
|--------------------|----------------------------------------|
| **Name**           | Gate Operation Logging                 |
| **Input**          | Gate operations performed              |
| **Process**        | System logs operations into database   |
| **Output**         | Operations stored for future retrieval |
| **Error Handling** | Show “unable to log operation” message |

### FR-18: Log Download and Search

| **ID**             | FR-18                                    |
|--------------------|------------------------------------------|
| **Name**           | Log Download and Search                  |
| **Input**          | Operator requests logs                   |
| **Process**        | System retrieves logs and enables search |
| **Output**         | Operator can download and search logs    |
| **Error Handling** | Show “logs unavailable” message          |
