# Key User Flows

## 1. Submit an Incident

1. User signs in.
2. User opens the report form.
3. User describes the issue, location, category, and optional evidence.
4. AI may suggest a summary, category, priority, department, or possible duplicates.
5. User reviews and edits suggestions.
6. User submits the report.
7. Server validates and stores the report.
8. UI shows confirmation only after successful acceptance.
9. User opens the report to track progress.

**Failure paths:** validation error, upload failure, AI unavailable, network failure, duplicate suggestion ignored, submission rejected. Provide clear recovery actions and never falsely show success.

## 2. Administrator Triage

1. Administrator opens the incident queue.
2. Filters or searches reports.
3. Opens a report and reviews details and AI suggestions.
4. Checks possible duplicates.
5. Confirms or changes category and priority.
6. Assigns a department or maintenance team.
7. Updates status and leaves an audit trail.
8. Reporter receives an update if notifications are enabled.

## 3. Maintenance Resolution

1. Team member opens the assigned work queue.
2. Reviews issue details and location.
3. Marks work as in progress.
4. Adds progress notes as needed.
5. Completes work and submits a resolution note.
6. Authorized reviewer verifies closure if required.
7. Incident status and history are updated.

## 4. Review a Possible Duplicate

1. Admin opens duplicate review.
2. Compares descriptions, locations, timestamps, and status.
3. Chooses whether reports are separate or duplicates.
4. If merged or linked, preserve history and reference the primary incident.
5. Inform affected users where appropriate.

## Flow Design Notes

- Use visible progress and status labels.
- Provide back navigation without losing entered data.
- Confirm consequential actions.
- Keep AI recommendations editable and distinguish them from confirmed decisions.
