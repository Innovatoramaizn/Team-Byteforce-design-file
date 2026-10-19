# SignalLoop

**From report to resolution.**

SignalLoop is an AI-assisted campus incident management platform designed to help students and staff report campus problems and help campus teams track, assign, and resolve them.

## UI/UX Design

Explore the editable Figma designs: [SignalLoop in Figma](https://www.figma.com/design/nXSDkSccAbuelYpk6gBwSg)

> The Figma file contains screen designs. Authentication, AI processing, notifications, offline sync, and incident workflows must be implemented and tested separately.

## Core Capabilities

- Campus incident reporting
- AI-assisted categorization, summarization, and priority suggestions
- Possible duplicate report suggestions
- Incident tracking and status updates
- Department assignment and maintenance work queues
- Administrative dashboards and analytics
- Optional voice-to-text reporting

AI recommendations are decision support; authorized people should be able to review and edit them.

## User Roles

- **Student or staff reporter:** creates reports and follows progress
- **Campus administrator:** reviews, prioritizes, assigns, and monitors incidents
- **Maintenance team:** views assigned work and records progress or resolution

## Brand and Design System

| Token | Value | Intended use |
|---|---|---|
| Deep Navy | `#101D33` | Primary brand, headings, navigation |
| Signal Teal | `#16B8A6` | Primary actions and progress |
| Intelligence Blue | `#6D9DFF` | AI suggestions and information accents |
| Cloud Grey | `#F4F7FB` | App background |
| White | `#FFFFFF` | Cards and forms |
| Charcoal | `#1E293B` | Primary text |
| Slate Grey | `#6B788B` | Secondary text |
| Soft Grey | `#E2E8F0` | Borders and dividers |
| Success Green | `#16A36A` | Resolved/success states |
| Warning Amber | `#F5A623` | Review/warning states |
| Priority Red | `#DC4C4C` | Urgent/high-priority states |

**Typography:** Manrope for prominent headings; Inter for UI and body text.

## Documentation

- [Product overview](docs/product-overview.md)
- [Functional requirements](docs/functional-requirements.md)
- [UI design system](docs/ui-design-system.md)
- [User flows](docs/user-flows.md)
- [Technical architecture proposal](docs/technical-architecture.md)
- [Development roadmap](docs/roadmap.md)
- [Privacy, security, and accessibility](docs/privacy-security-accessibility.md)

## Suggested Repository Structure

```text
signalloop/
├── README.md
├── docs/
│   ├── product-overview.md
│   ├── functional-requirements.md
│   ├── ui-design-system.md
│   ├── user-flows.md
│   ├── technical-architecture.md
│   ├── roadmap.md
│   └── privacy-security-accessibility.md
├── screenshots/
├── assets/
└── src/                 # Add when frontend implementation begins
```

## Current Status

This starter package contains project documentation and a link to the Figma designs. It does not yet include a working frontend or backend implementation.

## Proposed Technology Stack

- **Frontend:** React or Next.js with Tailwind CSS
- **Backend and data:** Supabase or an equivalent service
- **AI services:** an API for optional categorization, summarization, duplicate suggestions, and voice transcription
- **Deployment:** a compatible hosting platform such as Vercel

These are proposed choices, not claims that integrations are already configured.

## Getting Started

1. Create a GitHub repository named `signalloop`.
2. Upload this folder's contents to the repository root.
3. Add exported Figma screenshots to `screenshots/` if you want visual previews.
4. When implementation begins, add frontend source code and update this README with setup, testing, and deployment instructions.

## Contributions

Describe the problem being solved, keep UI behavior accessible, and document new configuration. Never commit secrets, API keys, credentials, or real sensitive incident reports.

## License

No license has been selected yet. Add a `LICENSE` file before granting others permission to reuse or redistribute this project.
