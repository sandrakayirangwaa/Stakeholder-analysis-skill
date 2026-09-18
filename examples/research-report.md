# Research Report: Customer Portal Usage & Operational Findings

**Project:** NextGen Customer Portal Upgrade
**Date:** September 2026

Summary: Operational monitoring and user research indicate the portal's checkout flow and authentication experience are the primary pain points driving support volume and conversion loss. The following findings synthesize logs, support tickets, and a small sample of user interviews.

Key findings:
- Performance: Median page load for checkout is ~1.8s; 95th percentile spikes to 8–12s during peak windows (evenings UTC), correlating with higher abandonment.
- Authentication: Intermittent auth session drops affect ~1.5% of login attempts, often tied to token refresh failures after the legacy SSO change.
- Billing errors: 40% of recent billing-related tickets trace to reconciliation delays during nightly batch processing.
- Conversion: Checkout drop-off is ~12% overall, consistent with analytics in the PRD; usability issues in the new flow account for a substantial portion of this loss.
- Support capacity: Customer support forecasts a 25–40% surge in tickets following rollout unless training and tooling are provided.

Operational constraints:
- Payment gateway must remain available 24/7 — zero-downtime migration is required.
- Global data compliance requires review of any changes to authentication and billing data flows.

Implications for the project:
- Prioritize backend migration and auth hardening in Phase 1 to reduce outage and compliance risk.

Sources: internal logs, support ticket triage summaries, and five user interviews with frequent checkout users.
