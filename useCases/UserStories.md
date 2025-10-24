# User Stories

Document capturing all main user stories covered. See [Glossary](./Dictionary.md) for definitions and conventions.

User stories are separated by Actors.

## Actors

- **Visitors**: incoming drivers, technicians, and visitors.
  - **Registered Visitors**: regular drivers/visitors/employees.
- **Gate Operator**: forklift operators, on-site staff
- **Office Staff**: warehouse staff, managers

## Visitors

- As a Visitor, I want to...
  - access the system through a QR code ([US-01](#us-01-visitor-qr-code-scan))
  - set the language of my preference for the content of the application ([US-02](#us-02-set-application-language))
  - be informed of the required security elements to enter the site ([US-03](#us-03-get-security-information))
  - be able to bypass filling the form if I am a regular visitor ([US-04](#us-04-choose-to-bypass-form))
  - fill in the required form for entrance ([US-05](#us-05-fill-in-entrance-form))
  - be notified of where I need to park when I enter the facility ([US-06](#us-06-receive-response-with-information))
  - be notified and redirected if I am in the wrong gate ([US-07](#us-07-redirection-to-correct-address))

To be added as needed:

- be notified when the operator views my application
- have the option to register as a regular visitor

## Gate Operator

- As a Gate Operator, I want to...
  - be notified when a new Visitor sends a form [US-08](#us-08-notification-of-incoming-visitor)
  - receive the form translated to Dutch (if necessary) [US-09](#us-09-receive-translated-form)
  - review the form and accept/deny it [US-10](#us-10-approvedeny-form)
  - send a response to the driver including where they need to park [US-10](#us-10-approvedeny-form)
  - open the gate [US-11](#us-11-open-gate)

## Office Staff

- As a Manager, I want to...
  - access logs of the gate's opening [US-12](#us-12-access-gate-logs)
  - obtain data for further analysis [US-13](#us-13-obtain-data-for-analysis)

## User Story Descriptions

### US-01: Visitor QR Code Scan

| **ID:**                  | US-01                                                                |
|--------------------------|----------------------------------------------------------------------|
| **Actor:**               | Visitor                                                              |
| **Description:**         | As a visitor, I want to scan a QR code so that I can request access. |
| **Acceptance Criteria:** | QR code is recognized, visitor is redirected to form.                |
| **Linked Use Cases:**    | [UC-01](UseCases.md#uc-01-request-facility-access)                 |

### US-02: Set Application Language

| **ID:**                  | US-02                                                                                                   |
|--------------------------|---------------------------------------------------------------------------------------------------------|
| **Actor:**               | Visitor                                                                                                 |
| **Description:**         | As a visitor, I want to choose the language the application is in.                                      |
| **Acceptance Criteria:** | The system and its components are translated to the selected language.                                  |
| **Linked Use Cases:**    | [UC-01](UseCases.md#uc-01-request-facility-access) <\br> [UC-05](UseCases.md#uc-05-choose-language) |

### US-03: Get Security Information

| **ID:**                  | US-03                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------|
| **Actor:**               | Visitor                                                                                  |
| **Description:**         | As a visitor, I want to be informed of the required security elements to enter the site. |
| **Acceptance Criteria:** | Application shows a list of security elements that must be worn inside the facility.     |
| **Linked Use Cases:**    | [UC-01](UseCases.md#uc-01-request-facility-access)                                     |

### US-04: Choose To Bypass Form

| **ID:**                  | US-04                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| **Actor:**               | Visitor                                                                                                          |
| **Description:**         | As a visitor, I want to be able to skip filling the form if I already know what to do/come to the site regularly |
| **Acceptance Criteria:** | Visitor is able to request access without filling in the form.                                                   |
| **Linked Use Cases:**    | [UC-10](UseCases.md#uc-10-regular-visitor)                                                                     |

### US-05: Fill In Entrance Form

| **ID:**                  | US-05                                                           |
|--------------------------|-----------------------------------------------------------------|
| **Actor:**               | Visitor                                                         |
| **Description:**         | As a visitor, I want to fill in the required form for entrance. |
| **Acceptance Criteria:** | Visitor is able to complete and submit the form.                |
| **Linked Use Cases:**    | [UC-01](UseCases.md#uc-01-request-facility-access)            |

### US-06: Receive Response with Information

| **ID:**                  | US-06                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------|
| **Actor:**               | Visitor                                                                                        |
| **Description:**         | As a visitor, I want to receive the operator's response with information such as where to park |
| **Acceptance Criteria:** | Response form is sent, visitor is directed to the appropriate parking location                 |
| **Linked Use Cases:**    | [UC-01](UseCases.md#uc-01-request-facility-access)                                           |

### US-07: Redirection to Correct Address

| **ID:**                  | US-07                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------|
| **Actor:**               | Visitor                                                                                             |
| **Description:**         | As a visitor, I want to be redirected to the correct gate if I'm in the wrong address               |
| **Acceptance Criteria:** | Visitor is notified they're in the wrong address, and instructions are shown to redirect the driver |
| **Linked Use Cases:**    |                                                                                                     |

### US-08: Notification of Incoming Visitor

| **ID:**                  | US-08                                                                                                        |
|--------------------------|--------------------------------------------------------------------------------------------------------------|
| **Actor:**               | Gate Operator                                                                                                |
| **Description:**         | As a gate operator, I want to be notified when a Visitor sends a form                                        |
| **Acceptance Criteria:** | Gate Operator is notified when a Visitor has submitted a form (or requested access, if they bypass the form) |
| **Linked Use Cases:**    | [UC-07](UseCases.md#uc-07-review-form)                                                                     |

### US-09: Receive Translated Form

| **ID:**                  | US-09                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------|
| **Actor:**               | Gate Operator                                                                                    |
| **Description:**         | As a gate operator, I want to receive forms filled in another language in Dutch                  |
| **Acceptance Criteria:** | Form received by Gate Operator is translated to Dutch (if it was filled in a different language) |
| **Linked Use Cases:**    | [UC-07](UseCases.md#uc-07-review-form) <br> [UC-05](UseCases.md#uc-05-choose-language)       |

### US-10: Approve/Deny Form

| **ID:**                  | US-10                                                                       |
|--------------------------|-----------------------------------------------------------------------------|
| **Actor:**               | Gate Operator                                                               |
| **Description:**         | As a gate operator, I want to review the form submitted and accept/deny it. |
| **Acceptance Criteria:** | Gate Operator can review the submitted form and send back a message         |
| **Linked Use Cases:**    | [UC-08](UseCases.md#uc-08-approvereject-visitor)                          |

### US-11: Open Gate

| **ID:**                  | US-11                                                          |
|--------------------------|----------------------------------------------------------------|
| **Actor:**               | Gate Operator                                                  |
| **Description:**         | As a gate operator, I want to be able to open the gate         |
| **Acceptance Criteria:** | Gate Operator can open gate on command, even without a request |
| **Linked Use Cases:**    | [UC-09](UseCases.md#uc-09-open-gate)                         |

### US-12: Access Gate Logs

| **ID:**                  | US-12                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------|
| **Actor:**               | Manager                                                                                           |
| **Description:**         | As a Manager, I want to access logs of the gate's opening so that I can review all access events. |
| **Acceptance Criteria:** | Manager can view, filter, and export gate opening logs.                                           |
| **Linked Use Cases:**    |                                                                                                   |

### US-13: Obtain Data for Analysis

| **ID:**                  | US-13                                                                                              |
|--------------------------|----------------------------------------------------------------------------------------------------|
| **Actor:**               | Manager                                                                                            |
| **Description:**         | As a Manager, I want to obtain data from gate operations and visitor entries for further analysis. |
| **Acceptance Criteria:** | Manager can generate reports and export data for analytical purposes.                              |
| **Linked Use Cases:**    |                                                                                                    |
