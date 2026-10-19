# Functional Requirements

These requirements describe intended behavior and should be refined with campus stakeholders before production use.

## Reporter Experience

### Sign in
- Allow an authorized user to authenticate.
- Display clear validation and recovery states.
- Apply role-based access after authentication.

### Create a report
- Capture a title or description, category, location, and optional supporting media.
- Allow users to review and edit AI-generated structure before submitting.
- Communicate required fields and validation errors.
- Preserve drafts if draft storage is implemented.
- Show a server-confirmed receipt only after the server accepts the submission.

### AI assistance
- Suggest a category and short summary.
- Suggest a priority and responsible department.
- Show possible duplicate reports when useful.
- Allow users or authorized reviewers to correct suggestions.
- Handle unavailable AI services gracefully without blocking manual reporting.

### Track reports
- Show status, timestamps, assigned team where appropriate, and status history.
- Provide loading, empty, failure, and retry states.
- Avoid exposing private reporter details to unauthorized users.

### Notifications
- Notify users about meaningful status changes when notification channels are implemented.
- Provide preferences where appropriate.
- Do not claim delivery unless delivery status is known.

## Administrator Experience

- View, filter, and search incident reports.
- Filter by status, category, priority, location, and department.
- Review AI suggestions and possible duplicates.
- Assign a department or maintenance team.
- Change priority and status with an audit trail.
- Review analytics on volume, status, and resolution time.

## Maintenance Experience

- View assigned incidents.
- See location, issue details, priority, and relevant attachments.
- Record progress notes and status changes.
- Submit a resolution note and evidence if required.
- Maintain a history of updates.

## System Requirements

- Enforce permissions on the server, not only in the UI.
- Validate and sanitize user input.
- Log important administrative actions.
- Provide accessible form labels, focus states, and error messages.
- Support mobile, tablet, and desktop layouts.
- Test offline and synchronization behavior before advertising it as supported.
