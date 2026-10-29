# Testing

Evidence date: October 29, 2026 (America/New_York). These results come from earlier recorded runs. The five-project package refresh reviewed the receipts and original-file hashes; it did not rerun application tests, lint or builds. Tests ran in isolated private copies using existing installed dependencies; no dependency reinstall was performed. JavaScript checks used Node 24.22.1.

| Check | Result |
|---|---|
| Vitest | 32 tests in 8 files passed |
| Production webpack build | PASS |
| ESLint | PASS with 2 internal-navigation warnings |
| npm dependency audit | 0 reported vulnerabilities; historical 19-entry result is superseded |

## Historical evidence

Older handoff reports were used as context, not counted as new test runs.

## Reproducibility and limits

The source is private, so these tests cannot be run from this documentation repository. The owner retains command receipts and redacted logs separately. Tests used fixtures/mocks without production credentials. No database migration, real email or Discord operation was authorized or executed.

Live Supabase accounts, database migrations and SMTP were not exercised. Existing guest submissions still return a service failure on any getUser authentication error; the missing-session path needs integration testing and remediation before a public demo. The historical narrow-screen validation overflow remains unverified. Localization, administrative UI depth and assistive-technology testing remain incomplete.

A dependency audit is a dated registry observation, not proof of exploitability or a security certification. No coverage percentage is claimed. [Overview](../README.md).
