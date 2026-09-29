# T4 — Scope Agreement

## 1. Committed Scope

Our team has two members and approximately two sprints remaining. To keep the project realistic, we are committing to a small number of features that can be completed, tested, and demonstrated by Session 26.

### 1. View Service Status

Users will be able to view the current status of a monitored service.

The service will display one of the following statuses:

* Operational
* Degraded
* Down

The team will demonstrate that a service's current status can be viewed through the system.

**T2 Traceability:** FR-1, FR-2
**Related User Story:** US-1

### 2. Basic Incident Management

Authorized team members will be able to create, update, and resolve incidents.

An incident will include basic information such as:

* Affected service
* Description
* Root cause
* Notes
* Ticket number

The team will demonstrate creating an incident, updating its information, and resolving the incident.

**T2 Traceability:** FR-6, FR-7, FR-8, FR-9
**Related User Stories:** US-4, US-5, US-6, US-7

### 3. Incident History

The system will store previous incidents so authorized team members can view past incidents and their information.

The team will demonstrate creating an incident and then viewing that incident in the incident history.

**T2 Traceability:** FR-10
**Related User Story:** US-8

### 4. Basic AI Incident Summary

A team member will be able to request an AI-generated summary of an incident using the available incident information.

The generated summary will be presented to a team member for review before it can be used as final incident information.

The team will demonstrate generating an incident summary and reviewing the generated result.

**T2 Traceability:** FR-16, FR-17, FR-18
**Related User Stories:** US-11, US-12

---

## 2. Explicitly Deferred Functionality

Because our team has two members and limited time remaining, we are intentionally deferring the following functionality:

### Automated Service Monitoring

We will not commit to automatic health checks based on configurable schedules.

**Deferred T2 Requirements:** FR-3, FR-4

### Manual Health Checks

We will not commit to implementing the manual health-check feature as part of the final scope.

**Deferred T2 Requirement:** FR-5

### Subscriber Notifications

We will not commit to implementing subscriber notification methods during the remaining sprints.

This includes:

* Notification method selection
* Email notifications
* Microsoft Teams notifications
* Text message notifications
* Automatic notifications when a service becomes Degraded or Down

**Deferred T2 Requirements:** FR-11, FR-12, FR-13, FR-14, FR-15

These features may be considered for a future version but are not part of our committed Session 26 scope.

---

## 3. Traceability

| Committed Item            | T2 Requirements        | T2 User Stories        |
| ------------------------- | ---------------------- | ---------------------- |
| View Service Status       | FR-1, FR-2             | US-1                   |
| Basic Incident Management | FR-6, FR-7, FR-8, FR-9 | US-4, US-5, US-6, US-7 |
| Incident History          | FR-10                  | US-8                   |
| Basic AI Incident Summary | FR-16, FR-17, FR-18    | US-11, US-12           |

Every committed feature is directly connected to a requirement from T2.

---

## 4. Delivery Risks

The main risks to completing the committed scope are:

* Only having two team members.
* Limited development time remaining.
* Bugs during testing.
* Difficulty integrating the AI feature.
* Time needed for the final demonstration and documentation.

## 5. Cut Order

If the team falls behind schedule, features will be removed in the following order:

1. AI incident summary.
2. Nonessential incident interface details.
3. Incident history functionality.
4. Basic incident management functionality, only if necessary.

The team will keep the basic service status display and basic incident management as the core of the project.

## Final Commitment

Our team is committing to demonstrating four core areas by Session 26: viewing service status, basic incident management, incident history, and a basic AI incident summary with human review.

We are intentionally deferring automated monitoring, manual health checks, and subscriber notifications because the team has two members and only two sprints remaining. This smaller scope gives the team a realistic amount of work that can be completed, tested, and demonstrated.
