# UI Design System

## Brand

- **Name:** SignalLoop
- **Tagline:** From report to resolution.
- **Category:** AI-assisted campus incident management
- **Personality:** trustworthy, intelligent, responsive, inclusive

## Color Tokens

| Token | Hex | Usage |
|---|---|---|
| `brand-navy` | `#101D33` | Primary brand, navigation, headings |
| `brand-teal` | `#16B8A6` | Primary actions and progress |
| `accent-blue` | `#6D9DFF` | AI information and highlights |
| `background` | `#F4F7FB` | Main app canvas |
| `surface` | `#FFFFFF` | Cards and form surfaces |
| `text-primary` | `#1E293B` | Main text |
| `text-secondary` | `#6B788B` | Supporting text |
| `border` | `#E2E8F0` | Borders and dividers |
| `success` | `#16A36A` | Resolved and success states |
| `warning` | `#F5A623` | Review and warning states |
| `danger` | `#DC4C4C` | Urgent or destructive states |
| `ai-surface` | `#E8F0FF` | AI suggestion panel background |
| `success-surface` | `#E4F8EF` | Success panel background |

Use color alongside labels or icons; never communicate status through color alone. Check contrast before implementation.

## Typography

- **Headings:** Manrope, bold or semibold
- **Body and interface:** Inter, regular or medium
- **Suggested desktop page title:** 28–32 px
- **Section heading:** 18–22 px
- **Body text:** 14–16 px
- **Labels:** 12–14 px
- **Metadata:** 11–12 px, only when comfortably readable

## Responsive Reference Breakpoints

- Small mobile: 320–374 px
- Mobile: 375–767 px
- Tablet: 768–1023 px
- Laptop: 1024–1439 px
- Desktop: 1440 px and above

Prefer mobile-first layouts for reporting. Keep forms short and avoid relying on hover for essential actions.

## Reusable Components

Create components and variants for:
- Buttons: primary, secondary, outline, destructive, disabled, loading
- Inputs: default, focused, invalid, disabled
- Status badges: submitted, under review, assigned, in progress, resolved, rejected
- Priority badges: low, medium, high, urgent
- Incident cards and tables
- AI suggestion panels with explicit review/edit affordances
- Empty, loading, error, offline, and success states
- Dialogs, confirmation prompts, toast messages, and navigation

## Voice and Language

Use clear, plain language. Consider Nigerian Pidgin as an accessible language option alongside English, and test copy with intended users. Voice input should remain optional and transcripts editable.

## Figma Handoff

Figma file: https://www.figma.com/design/nXSDkSccAbuelYpk6gBwSg

Suggested page organization:
1. Cover
2. Foundations
3. Components
4. Student experience
5. Admin experience
6. Maintenance experience
7. Prototype flows
8. Responsive layouts
9. Developer handoff
