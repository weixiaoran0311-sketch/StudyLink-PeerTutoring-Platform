# Use Case Descriptions - Analysis Phase

This document details the main and alternative flows for the core use cases in StudyLink, based on the Use Case Diagram created in the Planning phase. The flows are prioritized according to the Product Backlog and focus on high-value interactions.

## 1. Post Tutoring Request (Actor: Freshman Student)

**Main Flow**:
1. Freshman logs in to the system using student email and password.
2. Freshman navigates to the "Post Request" section from the dashboard.
3. System displays the tutoring request form.
4. Freshman enters required fields: subject code, topic, description, preferred time slot.
5. Freshman clicks "Submit".
6. System validates input (all required fields filled, valid format).
7. System creates the request and adds it to the public board.
8. System shows confirmation message: "Request posted successfully".
9. Freshman is redirected to view their posted requests or the public board.

**Alternative Flows**:
- 6a. If required fields are missing → system highlights errors and returns to form (step 3).
- 6b. If preferred time is in the past → system shows error and returns to form.

## 2. Assign Self to Request (Actor: Senior Student)

**Main Flow**:
1. Senior logs in to the system.
2. Senior navigates to the public requests board.
3. System displays list of open requests.
4. Senior selects a request to view details.
5. Senior clicks "Assign Myself".
6. System assigns the senior as tutor for the request.
7. System updates request status to "Assigned".
8. System shows confirmation: "You have been assigned as tutor".
9. Senior is redirected to the board or their tutoring history.

**Alternative Flows**:
- 3a. If no open requests → system shows "No requests available".
- 5a. If request already assigned → system disables button and shows "Already taken".

## 3. Update Request Status (Actor: Assigned Tutor / Senior)

**Main Flow**:
1. Tutor logs in and navigates to assigned requests or request detail page.
2. System displays current request details and status.
3. Tutor selects new status (e.g., "In Progress", "Completed").
4. Tutor clicks "Update Status".
5. System saves the change and updates the request.
6. System shows "Status updated successfully".
7. Freshman can now see the updated status in their request list.

**Alternative Flows**:
- 3a. Invalid status transition → system prevents update and shows error.

These flows provide detailed specifications for prototype implementation and testing, ensuring consistency with the Use Case Diagram and Product Backlog.
