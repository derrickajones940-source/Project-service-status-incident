
# Service Status and Incident Project
## Requirements Specification v1.0

---
# 1. Stakeholders
### Service Users
- **Interest:** Know if a service is working.
- **Influence:** Medium.
- **Need:** A clear view of the current service status.

### Operations/Support Team
- **Interest:** Find and respond to service problems.
- **Influence:** High.
- **Need:** Alerts, service status, and incident information.

### Developers
- **Interest:** Find and fix service problems.
- **Influence:** High.
- **Need:** Monitoring information and incident details.

### Project Team
- **Interest:** Build and maintain the system.
- **Influence:** High.
- **Need:** Clear requirements and testable features.

### Project Management
- **Interest:** Understand service problems and incidents.
- **Influence:** Medium.
- **Need:** Service status and incident information.

---

# 2. Functional Requirements
## Service Monitoring

**1.** The system shall show the current status of each monitored service.
**2.** The system shall show services as:
- Operational
- Degraded
- Down

## Incident Management

**3.** The system shall allow an authorized team member to create an incident.
**4.** An incident shall include:
- Affected service
- Description
- Root cause
- Notes
- Ticket number

**5.** The system shall allow authorized team members to update an incident.
**6.** The system shall allow authorized team members to mark an incident as resolved.
**7.** The system shall keep a history of previous incidents.

## Notifications

**8.** The system shall notify designated team members when a service becomes Degraded or Down.

## AI Assistance

**9.** The system shall allow a team member to request an AI-generated incident summary.
**10.** A team member shall review an AI-generated summary before it is used as final incident information.

---

# 3. Non-Functional Requirements

**NF-1.** The system shall display a requested service status within **3 seconds**.
**NF-2.** The system shall check each monitored service at least **once every 60 seconds**.
**NF-3.** The system shall send a notification within **60 seconds** after detecting a Degraded or Down condition.
**NF-4.** The system shall keep incident records for at least **30 days**.
**NF-5.** Only authorized team members shall be able to create, update, or resolve incidents.
**NF-6.** Each implemented functional requirement shall have at least **one test case**.

---

# 4. Epics and User Stories
## Epic 1: Service Monitoring
### US-1.: View Service Status

**Story:**  
As a service user, I want to see the current service status so I know if it is working.

**Acceptance Criteria:**
- Operational services show "Operational."
- Degraded services show "Degraded."
- Down services show "Down."

### US-2. Identify Service Condition

**Story:**  
As an operations team member, I want the system to identify service problems so I know when action is needed.

**Acceptance Criteria:**
- The system checks the service.
- The system identifies the correct status.
- The status follows the project's monitoring rules.

---

## Epic 2: Incident Management

### US-3.: Create an Incident

**Story:**  
As an operations team member, I want to create an incident so a service problem can be recorded.

**Acceptance Criteria:**
- An authorized team member can create an incident.
- The affected service is recorded.
- The incident is saved.

### US-4: Add Incident Details

**Story:**  
As an operations team member, I want to add details to an incident so other team members know what happened.

**Acceptance Criteria:**
- A description can be added.
- A root cause can be added.
- Notes can be added.
- A ticket number can be added.

### US-5: Update an Incident

**Story:**  
As an operations team member, I want to update an incident so the information stays current.

**Acceptance Criteria:**
- An authorized team member can update the incident.
- The updated information is saved.

### US-6: Resolve an Incident

**Story:**  
As an operations team member, I want to resolve an incident when the problem is fixed.

**Acceptance Criteria:**
- An authorized team member can resolve the incident.
- The incident shows as resolved.
- The incident remains in the history.

### US-7: View Incident History

**Story:**  
As an operations team member, I want to view previous incidents so I can review past problems.

**Acceptance Criteria:**
- Previous incidents can be viewed.
- Incident details are displayed.
- Resolved incidents remain in the history.

## Epic 3: Notifications

### US-8: Degraded Notification

**Story:**  
As an operations team member, I want to receive a notification when a service becomes degraded so I can investigate it.

**Acceptance Criteria:**
- A notification is sent when the Degraded condition occurs.
- The notification identifies the affected service.
- The notification shows the service status.

### US-9: Down Notification

**Story:**  
As an operations team member, I want to receive a notification when a service goes down so I can respond.

**Acceptance Criteria:**
- A notification is sent when the Down condition occurs.
- The notification identifies the affected service.
- The notification shows the service status.

---

## Epic 4: AI Assistance

### US-10: Generate AI Summary

**Story:**  
As an operations team member, I want AI to summarize an incident so I can understand the important information faster.

**Acceptance Criteria:**
- A team member can request a summary.
- The summary uses the incident information.
- The summary is identified as AI-generated.

### US-11: Review AI Summary

**Story:**  
As an operations team member, I want to review the AI summary so incorrect information is not accepted.

**Acceptance Criteria:**
- A team member reviews the summary.
- The team member can make changes.
- The team member decides whether the summary is acceptable.

---

# 5. Traceability
The traceability table connects:

**Charter Goal → Requirement → User Story**

| Charter Goal | Requirement | User Story |
|---|---|---|
| Monitor services | FR-1, FR-2 | US-1, US-2 |
| Manage incidents | FR-3, FR-4, FR-5, FR-6 | US-3, US-4, US-5, US-6 |
| Keep incident history | FR-7 | US-7 |
| Notify team members | FR-8 | US-8, US-9 |
| Use AI for incident assistance | FR-9 | US-10 |
| Keep humans involved in AI decisions | FR-10 | US-11 |

### Non-Functional Requirements

| Requirement | Related User Story |
|---|---|
| NF-1 | US-1 |
| NF-2 | US-2 |
| NF-3 | US-8, US-9 |
| NF-4 | US-7 |
| NF-5 | US-3, US-5, US-6 |
| NF-6 | All applicable stories |

---

# 6. Gaps and Conflicts
- Does every charter goal have at least one requirement?
- Does every requirement connect to a user story?
- Does every user story connect to a requirement?
- Are any requirements outside the project scope?
- Are any requirements missing?
- Are the requirements and user stories consistent with each other?

# 7. Authorship
- Stakeholder Analysis — [Karen]
- Functional Requirements — [Derricka]
- Non-Functional Requirements — [Derricka]
- Epics — [Karen]
- User Stories — [Karen]
- Acceptance Criteria — [Derricka]
- Traceability — [Karen]
- Gaps and Conflicts — [Derricka]
- AI Disclosure — [Karen-Derricka]
# 8. AI-Use Disclosure

The team used ChatGPT to help brainstorm requirements, organize user stories, improve wording, and check for possible gaps.
The team reviewed the AI suggestions and made the final decisions about the requirements.
AI was used as a support tool and did not make the final project decisions.

(AI Tool Use)
ChatGPT - Brainstorming 
ChatGPT - Requirement wording 
ChatGPT - User story organization 
ChatGPT - Traceability checking
ChatGPT - Finding possible gaps 
