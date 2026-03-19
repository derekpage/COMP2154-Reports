# Weekly Progress Report 2

### Derek Page

## 1. Executive Summary / This Week in Brief

During the past week, I focused on addressing the backlog of issues which have cause the back-end tasks to fall behind the front-end tasks. In particular, the issues relating to how the project will handle image uploads and editing. I also started developing a formal testing strategy to ensure that the completed back-end tasks for authentication and item CRUD operations meet the defined requirements. Additionally, I reviewed and assigned tasks from the upcoming epic, looking to identify potential areas where problems could arise that impact the teams ability to complete the tasks efficiently.

## 2. Testing Strategy

The primary testing strategy for the back-ends functionality involves unit testing to ensure that the individual functions perform as intended, integration testing to verify that the API will respond correctly to HTTP requests in the required way, as well as overall system-level testing alongside the front-end to ensure that the functionality of the project will meet the requirements defined in previous reports.

## 3. Initial Test Plan

The initial test plan is intended to ensure that the behavior of key features such as authentication and item post/listing meet the defined requirements. I have written out test cases to cover a wide variety of scenarios to try and address any possible edge cases which should be prioritized if an issue arises. These test cases have clearly defined conditions and requirements in order to ensure that the tests can be done efficiently and effectively.

## 4. Version Control and Integration

Our team has been using Git for version control of the project, with features developed on their own branches before merging with the main branch. The teams goal when performing these merges is to ensure that the main branch remains stable and minimizes the presence of critical bugs

## 5. Milestones and Completed Work

- Began work on assigned tasks for claim and verification features.
- Mapped out routes needed for upcoming epic to implement with placeholder data returned before the actual tasks are able to be completed.
- Assigned tasks for back-end team to complete during upcoming epic.
- Developed high-level testing plan to address existing back-end features of the project such as authentication and item CRUD operations.

## 6. Work in Progress

- Started to address the issue with back-end handling of image uploads and static hosting.

## 7. Blockers and Risks

| Risk | Level | Description | Mitigation |
|----|----|----|----|
| Front-end Back-end coordination | Medium | Front-end team is far ahead of back-end team's progress through the defined epics | |
| Other Obligations | High | Work on project needs to be balanced alongside school and person obligations to ensure that no areas suffer | Better time management to ensure tasks are consistently addressed |

## 8. Plan for Next Week

- Complete assigned tasks  for claim and verification features.
- Start to complete tasks as defined in epic 4 on Jira
- Continue work to address the issue related to image upload/editing
- Start performing tests from the structured test plan to ensure existing features meet requirements

## 9. Architecture and Design Updates

- No updates

## 10. Project Management Updates

- Back-end tasks for epic 4 have been assigned

## 11. Implementation, Testing and Quality Updates

- Functionality of the authentication features has been informally tested with front-end and back-end working together
- The item CRUD operations on the back-end side has been informally tested using Postman to ensure the server responds as expected to various HTTP requests
- Formal back-end testing plan has been defined to provide better testing coverage

## 12. Reflection

The team has continued to make good progress towards the completion of the Lost and Found project. We are currently in the middle of our epic 3 in the timeline but there is functionality from epic 2 that is still not working as intended. We are also developing better structured testing plan to ensure that the existing features of the project performs as expected for a variety of test cases, ensuring that edge cases are covered efficiently.

## 13. Initial Test Cases (Back-End)

### Test Case 1 - Successful Lost Item Creation

| Test Case ID | TC-ITEM-001 |
|----|----|
| Test Case Name | Successful Lost Item Creation |
| Requirement Reference | FR-4 |
| Priority | High |
| Test Level | Unit |
| Test Type | Positive |
| Pre-Conditions | User is logged in |

Test Steps:
- Use Postman to send HTTP Post request to /api/items/ with body containing all required form fields
- Run mysql query to verify presence of new item in database

Expected Results:
- The server should respond with a 201 status code
- The item should be added into the database

### Test Case 2 - Item Not Found (Update Route)

| Test Case ID | TC-ITEM-002 |
|----|----|
| Test Case Name | Item Not Found (Update Route) |
| Requirement Reference | FR-5 |
| Priority | High |
| Test Level | Unit |
| Test Type | Negative |
| Pre-Conditions | User is logged in |

Test Steps:
- Use Postman to send HTTP Put request to /api/items/:id, where id does not correspond to any item in DB

Expected Results:
- The server should respond with a 404 status code