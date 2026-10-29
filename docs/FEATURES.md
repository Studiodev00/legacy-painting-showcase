# Verified features

- Service presentation, navigation, estimate intake and recruiting forms.
- English/Portuguese selection with persisted preference; some forms/private screens remain only partially localized.
- Authentication, protected customer estimate history and role-checked administration.
- Server validation, SQL migrations and row-level-security policies.
- CSV export with formula safeguards, delivery status and protected email retry are implemented.

## Evidence level

These capabilities were found in the private source and related local records. Execution receipts exist for the checks listed in [Testing](TESTING.md); this package refresh reviewed those records without rerunning the applications. Presence in code, enabled configuration and live operation are different claims.

## Limits

Live Supabase accounts, database migrations and SMTP were not exercised. Existing guest submissions still return a service failure on any getUser authentication error; the missing-session path needs integration testing and remediation before a public demo. The historical narrow-screen validation overflow remains unverified. Localization, administrative UI depth and assistive-technology testing remain incomplete.

## Visual evidence

Owner-approved historical local captures of the public homepage and empty estimate form. Client assets remain reserved for this presentation; no reuse license is granted.

[Overview and screenshots](../README.md).
