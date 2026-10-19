# Technical Architecture Proposal

This is a proposed architecture, not a record of an existing implementation.

## Suggested Stack

- **Frontend:** React or Next.js
- **Styling:** Tailwind CSS
- **Authentication and database:** Supabase or an equivalent managed backend
- **File storage:** protected object storage for incident attachments
- **AI services:** API integration for summarization, classification, duplicate suggestions, and optional speech transcription
- **Hosting:** a platform compatible with the selected frontend framework

## Conceptual Modules

- Identity and access
- Incident reports
- AI assistance
- Triage and assignment
- Maintenance workflow
- Notifications
- Analytics and audit events

## Initial Data Model

### `profiles`
- `id`
- `display_name`
- `role`
- `created_at`

### `incidents`
- `id`
- `reporter_id`
- `title`
- `description`
- `category`
- `location`
- `priority`
- `status`
- `department_id`
- `created_at`
- `updated_at`
- `resolved_at`

### `incident_updates`
- `id`
- `incident_id`
- `author_id`
- `status`
- `note`
- `created_at`

### `departments`
- `id`
- `name`
- `created_at`

### `incident_attachments`
- `id`
- `incident_id`
- `storage_path`
- `uploaded_by`
- `created_at`

### `audit_events`
- `id`
- `actor_id`
- `incident_id`
- `action`
- `metadata`
- `created_at`

Review this model with stakeholders. Add constraints, indexes, retention policies, and access rules before production.

## Security Requirements

- Enforce row-level and role-based permissions at the backend.
- Store secrets in environment variables or a secret manager, never in Git.
- Restrict access to attachments and private incident data.
- Validate file type, size, and permissions.
- Rate-limit sensitive endpoints.
- Record important administrative changes.
- Minimize personal data sent to AI services.
- Define retention and deletion policies.

## AI Integration Principles

- Treat model outputs as suggestions, not authoritative decisions.
- Validate structured outputs before using them.
- Provide manual fallbacks when AI is unavailable.
- Avoid sending sensitive information unless necessary and appropriately protected.
- Evaluate quality on representative campus reports before relying on suggestions.

## PWA and Offline Behavior

If offline support is implemented, define draft storage, pending submission sync, and conflict handling. Clearly distinguish local drafts from server-confirmed submissions. Test before claiming this capability.
