# Architecture

App Router pages and shared React components handle presentation. Server routes validate input, check permissions and persist records through Supabase clients. PostgreSQL migrations define data and policies. SMTP notification runs after persistence, with a separate delivery status and administrative retry path.

```text
Public pages/forms → server validation → Supabase/PostgreSQL → SMTP notification
Authenticated customer/admin → server authorization → scoped data or CSV export
```

## Design rationale

Shared schemas align client and server validation. Server-side roles and database policies complement UI restrictions. Persistence and notification are distinct outcomes, allowing a saved inquiry to survive a delivery failure.

## Boundaries

Live Supabase accounts, database migrations and SMTP were not exercised. Existing guest submissions still return a service failure on any getUser authentication error; the missing-session path needs integration testing and remediation before a public demo. The historical narrow-screen validation overflow remains unverified. Localization, administrative UI depth and assistive-technology testing remain incomplete.

The diagram is an explanatory abstraction of inspected source, not a deployment topology or operational runbook. [Overview](../README.md).
