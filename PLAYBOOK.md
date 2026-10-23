# Playbook: Service Status and Incident Project
**Version:** v0.3

---

## 1. Branching Strategy
- We will use a branch for each feature or task (each person works on their own change without changing the main project).
- Branch names should describe the work being completed.
- Branches must be merged within 7 days (the work should not stay separate for more than one week).
- Team members will not directly push unfinished work to main (the main branch should only contain completed work).

---

## 2. Quality Gates & Enforcement Tools

To maintain code quality and stability, all Python/Django code submitted to the repository must pass four mandatory quality gates.

| Gate Name | What It Checks | Concrete Tool | Execution Location | Failure Action |
| :--- | :--- | :--- | :--- | :--- |
| **Linting & Code Formatting** | Syntax errors, PEP 8 style violations, unused imports, and code formatting consistency. | `ruff` | Both (Local via developer terminal / pre-commit & CI via GitHub Actions) | **Local:** Prevents clean commit. <br>**CI:** Fails workflow job and **blocks Pull Request merge**. |
| **Static Type Checking** | Type correctness, improper function arguments, and Django model/ORMs typing using `django-stubs`. | `mypy` | Both (Local developer run & CI via GitHub Actions) | **Local:** Developer fixes type warnings. <br>**CI:** Fails workflow job and **blocks Pull Request merge**. |
| **Test Suite Execution** | Correctness of Django models, views, APIs, and business logic. | `pytest` (with `pytest-django`) | Both (Local development environment & CI test runner in GitHub Actions) | **Local:** Unsaved broken changes. <br>**CI:** Fails workflow job and **blocks Pull Request merge**. |
| **Security Static Analysis** | Common security vulnerabilities in Python code (e.g., hardcoded secrets, unsafe SQL queries, unsafe `eval` usage). | `bandit` | CI (GitHub Actions security job) | **CI:** Fails workflow job and **blocks Pull Request merge**. |

### Note on Code Coverage Floor
> **Status:** **Deferred to Amendment 1 (Session 15)**
> 
> A numeric code coverage percentage target (e.g., 80%) is **not** set in version v0.3. In accordance with the course roadmap, we will generate and review an actual coverage report (`pytest-cov`) for our codebase during session 15. A concrete numeric floor will be formally established and locked in **Amendment 1 at Session 15**, ensuring our target is based on empirical codebase metrics rather than guesswork.

---

## 3. Definition of Done
A task is done when:
- The work is completed (everything required for the task has been finished).
- The work has been tested (we checked that it works).
- Tests pass (all `pytest` checks and quality gates pass with no errors).
- The work has been reviewed by another team member (someone else checks the work).
- The pull request has been approved and merged into main (the team accepted the work and added it to the main project).

---

## 4. Sprint Length and Meetings
- Our sprints will be 2 weeks long (we will plan and work on tasks for two weeks at a time).
- We will meet at the beginning of each sprint to plan tasks (decide what everyone will work on).
- We will have one team check-in each week (everyone gives an update on their progress and any problems).
- At the end of each sprint, we will review our work (look at what we completed).
- We will also discuss what could be improved (talk about what went well and what we should change).

---

## 5. Pull Requests and Reviews
- All changes must use a pull request (a request to have your work added to the main project).
- Each pull request needs 1 approval from another team member (one teammate must look at and approve the work).
- The reviewer will check that the work meets the requirement, works correctly, and does not break existing work (make sure the change does what it is supposed to do without causing new problems).
- Review comments must be fixed before merging (if your teammate finds a problem, fix it before adding the work to main).
- If a pull request is not reviewed within 48 hours (2 days), the team member will remind the team.
- Pull requests cannot be merged until the required approval is received (you must have another teammate approve it first).

---

## 6. AI Tools and Use

### Approved Tools
- The team may use ChatGPT for brainstorming, explaining concepts, debugging help, documentation, and generating ideas.
- ChatGPT may be used to help write or improve code, but team members must understand and check any AI-generated code before using it.
- AI tools should not make final project decisions without review by a team member.
- Each team member is responsible for the work they submit, even when AI was used to help create it.

### Prompt Log Policy
- Significant AI use for the project will be recorded in an AI prompt log.
- The prompt log will be stored in the team repository.
- The log should include the date, team member, AI tool used, and the prompt or a short description of the prompt.
- Each team member is responsible for recording their own significant AI use.
- The prompt log will be updated when AI is used for significant code, documentation, design, or project decisions.
- Passwords, API keys, private information, or other sensitive information should not be entered into AI tools or the prompt log.

### AI-Assisted Code Review
- AI code review does not replace the required human code review.
- An AI tool may be used to find possible bugs, errors, security issues, or other problems in a pull request.
- Team members should review AI feedback and make appropriate changes when needed.
- The required approval from another team member is still necessary before a pull request can be merged.
- Human review is required because a team member must understand the code and take responsibility for the final approval.
