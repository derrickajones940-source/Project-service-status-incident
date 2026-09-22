
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

### Subscribers
- **Interest:** Receive updates when a service has a problem.
- **Influence:** Medium.
= **Need:** Notifications through their selected method (email, Teams, or text).

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
## Epic 1: Service Monitoring

- **FR-1.** The system shall show the current status of each monitored service.
- **FR-2.** The system shall show services as:
  - Operational
  - Degraded
  - Down
- **FR-3.** The system shall allow an authorized user to set health-check frequency for a monitored service.
- **FR-4.** The system shall automatically check each monitored service according to its configured frequency.
- **FR-5.** The system shall allow authorized engineering users to manually check a monitored service.

## Epic 2: Incident Management

- **FR-6.** The system shall allow an authorized team member to create an incident.
- **FR-7.** An incident shall include:
  - Affected service
  - Description
  - Root cause
  - Notes
  - Ticket number

- **FR-8.** The system shall allow authorized team members to update an incident.
- **FR-9.** The system shall allow authorized team members to mark an incident as resolved.
- **FR-10.** The system shall keep a history of previous incidents.

## Epic 3: Notifications

- **FR-11.** The system shall allow subscribers to select a supported notification method.
- **FR-12.** The system shall support email notifications.
- **FR-13.** The system shall support Microsoft Teams notifications.
- **FR-14.** The system shall support text messages
- **FR-15.** The system shall notify subscribers when a service becomes Degraded or Down.

## Epic 4: AI Assistance

- **FR-16.** The system shall allow a team member to request an AI-generated incident summary.
- **FR-17.** The AI generated summary shall use available incident information.
- **FR-18.** A team member shall review an AI-generated summary before it is used as final incident information.

---

# 3. Non-Functional Requirements

- **NF-1.** The system shall display a requested service status within **3 seconds**.
- **NF-2.** The system shall perform each configured health check within **10 seconds** of its scheduled check time.
- **NF-3.** The system shall send a notification within **60 seconds** after detecting a Degraded or Down condition.
- **NF-4.** The system shall keep incident records for at least **30 days**.
- **NF-5.** Only authorized engineering users shall be able to perform manual health checks or create, update, or resolve incidents.
- **NF-6.** Each implemented functional requirement shall have at least **one documented test case**.
- **NF-7.** An AI-generated incident summary shall not be saved as final incident information until an authorized team member has reviewed it.

---

# 4. Epics and User Stories
## Epic 1: Service Monitoring
### US-1: View Service Status

**Story:**  
As a service user, I want to see the current service status so I know if it is working.

**Acceptance Criteria:**
- Operational services show "Operational."
- Degraded services show "Degraded."
- Down services show "Down."

### US-2: Configure Health Checks
**Story:**
As an engineering user, I want to set how often a service is checked so monitoring fits the service's needs.

**Acceptance Criteria:**
- An authorized user can select a health-check frequency.
- The selected frequency is saved.
- The system checks the service according to the selected freqeuncy.

### US-3: Manually Check a System

**Story:**  
As an engineering user, I want to manually check a service so I can investigate a problem when needed.

**Acceptance Criteria:**
- Only authorized engineering users can perform manual checks.
- The system performs the health check.
- The result is displayed.

---

## Epic 2: Incident Management

### US-4: Create an Incident

**Story:**  
As an engineering user, I want to create an incident so a service problem can be recorded.

**Acceptance Criteria:**
- An authorized engineer user can create an incident.
- The affected service is recorded.
- The incident is saved.

### US-5: Add Incident Details

**Story:**  
As an engineering user, I want to add details to an incident so other team members know what happened.

**Acceptance Criteria:**
- A description can be added.
- A root cause can be added.
- Notes can be added.
- A ticket number can be added.

### US-6: Update an Incident

**Story:**  
As an engineering user, I want to update an incident so the information stays current.

**Acceptance Criteria:**
- An authorized engineering user can update the incident.
- The updated information is saved.

### US-7: Resolve an Incident

**Story:**  
As an engineering user, I want to resolve an incident when the problem is fixed.

**Acceptance Criteria:**
- An authorized team member can resolve the incident.
- The incident shows as resolved.
- The incident remains in the history.

### US-8: View Incident History

**Story:**  
As an engineering user, I want to view previous incidents so I can review past problems.

**Acceptance Criteria:**
- Previous incidents can be viewed.
- Incident details are displayed.
- Resolved incidents remain in the history.

## Epic 3: Notifications

### US-9: Select Notification Method

**Story:**  
As a subscriber, I want to select how I receive notifications so I can use my preferred method.

**Acceptance Criteria:**
- A subscriber can select a supported notification method.
- The selected method is saved.
- The system uses the selected method for notifications.

### US-10: Receive Service Notifications

**Story:**  
As a subscriber I want to receive a notification when a service becomes degraded or goes down so I know about the problem quickly.

**Acceptance Criteria:**
- A notification is triggered when a Degraded or Down condition is detected.
- The notification identifies the affected service.
- The notification shows the service status.
- The notification is sent using the subscriber's selected method.

---

## Epic 4: AI Assistance

### US-11: Generate AI Summary

**Story:**  
As an engineering user, I want AI to summarize an incident so I can understand the important information faster.

**Acceptance Criteria:**
- A team member can request a summary.
- The summary uses available incident information.
- The summary is identified as AI-generated.

### US-12: Review AI Summary

**Story:**  
As an engineering user, I want to review the AI summary so incorrect information is not accepted.

**Acceptance Criteria:**
- A team member reviews the summary.
- The team member can make changes.
- The team member decides whether the summary is acceptable.
- An unreviewed summary cannot be saved as final incident information.


---

# 5. Traceability
The traceability table connects:

**Charter Goal → Requirement → User Story**

| Charter Goal | Requirement | User Story |
|---|---|---|
| Monitor services | FR-1 - FR-5 | US-1 - US-3 |
| Manage incidents | FR-6 - FR-9 | US-4 - US-7 |
| Keep incident history | FR-10 | US-8 |
| Provide Notifications | FR-11 - FR-15 | US-9 - US-10 |
| Use AI for incident assistance | FR-16 - FR-17 | US-11 |
| Keep humans involved in AI decisions | FR-18 | US-12 |

### Non-Functional Requirements

| Charter Goal | Requirement | Related User Story |
|---|---|---|
| Easy-to-use interface | NF-1 | US-1 |
| Service monitoring | NF-2 | US-2, US-3 |
| Notifications sent ASAP | NF-3 | US-10 |
| Incident history | NF-4 | US-8 |
| Role-based access for engineering users | NF-5 | US-3, US-4, US-6, US-7, US-11, US-12 |
| Basic testing | NF-6 | All applicable stories |
| Easy-to-use interface | NF-7 | US-1
| Human review of AI summaries | NF-8 | US-12

---

# 6. Gaps and Conflicts
The requirements review identified the following items that still need to be resolved:
### Gap 1: Degraded Status
The stakeholder did not provide a specific rule for when a service should be classified as Degraded instead of Operational or Down.
- **Action:** The team will define measurable conditions for the Degraded status before implementation.
### Gap 2: Health-Check Frequency After Failure
The stakeholder questioned whether the system should change its checking frequency after detecting a failure.
- **Action:** The team will determine whether a failure changes the monitoring frequency or only changes the service status.
### Gap 3: Notification Implementation
The stakeholder requested email, Teams, and text notifications.
- **Action:** The team will confirm the technical feasibility of each notification method and document any limitations.
### Gap 4: Stakeholder Terminology
The original stakeholder responses refer to users, subscribers, and engineering staff somewhat interchangeably.
- **Action:** The project will use the following roles consistently:
  - **Service User:** Views service status and incident information.
  - **Subscriber:** Receives service notifications.
  - **Engineering User:** Manages services and incidents.
A person may have more than one role.

---

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

---

# 8. AI-Use Disclosure
The team used ChatGPT to help brainstorm requirements, organize user stories, improve wording, and check for possible gaps.
The team reviewed the AI suggestions and made the final decisions about the requirements.
AI was used as a support tool and did not make the final project decisions.

(AI Tool Use)
- ChatGPT - Brainstorming 
- ChatGPT - Requirement wording 
- ChatGPT - User story organization 
- ChatGPT - Traceability checking
- ChatGPT - Finding possible gaps 
