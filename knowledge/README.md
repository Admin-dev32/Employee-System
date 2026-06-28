# Internal Knowledge System

This folder is a simple internal knowledge and payment reference system.

It is for Jorge, the team, and future AI/Codex sessions to quickly understand company profiles, worker profiles, and compensation rules without building a database, HR platform, admin panel, or authentication system.

## Structure

- `companies/` — company profiles and company-level payment notes.
- `workers/` — worker profiles and the reusable worker profile template.
- `compensation/` — worker/company compensation rules, commission references, and the reusable compensation template.

## Current Companies

- Manna Snack Bars: `companies/manna-snack-bars.md`
- Bako Business Branding: `companies/bako-business-branding.md`

## Current Workers

- Fernando: `workers/fernando.md`

## Current Manna / Fernando References

- Manna company profile: `companies/manna-snack-bars.md`
- Fernando worker profile: `workers/fernando.md`
- Fernando compensation rules: `compensation/manna-fernando-compensation.md`
- Fernando commission calculator/reference: `compensation/manna-commission-calculator.md`
- Fernando commission examples: `compensation/manna-commission-examples.md`
- Payment rules index: `compensation/payment-rules-index.md`

## How to update this system

1. Keep updates simple and in Markdown.
2. Use `TODO` when information is unknown.
3. Do not invent payment amounts, rates, roles, supervisors, bonuses, or approval rules.
4. For a new worker, copy `workers/worker-template.md` and fill in only known details.
5. For a new compensation plan, copy `compensation/compensation-template.md` and fill in only approved payment details.
6. Link new worker files from the related company profile.
7. Link new compensation files from the related worker profile and `compensation/payment-rules-index.md`.
8. Do not copy Manna rules into another company unless Jorge specifically approves it.
9. If official Manna pricing changes, update the commission examples and any related reference notes.

## Notes

- This is for internal use only.
- Do not add a database, admin panel, authentication, or complex tooling here.
- Use `TODO` where information is unknown.
- Do not copy payment rules from one company to another unless specifically approved.
- Review and update relevant files when compensation rules, worker roles, or company policies change.

## Source Documents

- `Manna_Growth_Blueprint_(2).pdf` was requested as a source document, but it was not available in this repository at the time these files were created.

## Future updates needed from Jorge

- Confirm what month or period counts for commission stages.
- Confirm who is the official supervisor for discount approvals.
- Confirm if Bako Business Branding will use hourly pay, project pay, salary, commission, or mixed pay.
- Confirm if other workers should be added.
