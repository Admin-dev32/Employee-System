# Internal Payment Knowledge System Manual

## 1. What This System Is

This is a simple internal knowledge system for worker payment information.

It stores plain Markdown notes about:

- Worker profiles
- Company profiles
- Payment types
- Event commissions
- Fixed pay
- Salaries
- Bonuses
- Chargebacks and adjustments
- Approval rules
- Payment instructions

This system is meant to be easy for Jorge, future ChatGPT sessions, and Codex to read and safely update.

This system is NOT:

- A payroll app
- A legal HR system
- A database
- An accounting system
- A replacement for final owner approval

## 2. Main Goal

The main goal is to keep internal payment knowledge clear and safe to update.

Use this system to:

- Keep worker payment rules clear.
- Make sure ChatGPT/Codex does not invent payment information.
- Make it easy to add future workers.
- Make it easy to update commissions, fixed pay, salary, bonuses, and approval rules.
- Keep Manna Snack Bars and Bako Business Branding rules separate.

## 3. Folder Structure

### `knowledge/companies/`

- One file per company.
- Stores company profile information.
- Links to related worker profiles and payment rules.

Current files:

- `manna-snack-bars.md` — Manna Snack Bars company profile, links to Fernando, Manna/Fernando compensation rules, commission references, and the payment rules index.
- `bako-business-branding.md` — Bako Business Branding company profile placeholder. Payment details are currently TBD.

### `knowledge/workers/`

- One file per worker.
- Stores the worker's role, responsibilities, payment summary, restrictions, approval rules, and links to related files.

Current files:

- `fernando.md` — Fernando's worker profile for Manna Snack Bars.
- `worker-template.md` — reusable template to copy when adding future workers.

### `knowledge/compensation/`

- Stores the actual payment, commission, salary, bonus, chargeback, and adjustment rules.
- Stores calculation references and examples when commission rules need extra clarity.

Current files:

- `manna-fernando-compensation.md` — main Manna Snack Bars compensation rules for Fernando.
- `manna-commission-calculator.md` — simple human-readable commission calculator/reference for Fernando.
- `manna-commission-formula.md` — plain-language formula for Fernando's Manna commission.
- `manna-commission-examples.md` — rounded commission examples for Fernando.
- `compensation-template.md` — reusable template to copy when adding a future compensation plan.
- `payment-rules-index.md` — index of active and future payment rule files.

## 4. Current Active Worker: Fernando

Fernando is currently the first active worker profile for Manna Snack Bars.

Current known information:

- Company: Manna Snack Bars
- Fixed monthly payment: `$100/month`
- The fixed monthly payment is separate from event commissions.
- The original PDF showed `$40/month`, but the current active amount is `$100/month`.
- Event commission is calculated separately using the Manna/Fernando commission rules.

## 5. How Fernando's Manna Payment Works

Fernando's current Manna compensation has two separate parts.

### Part 1: Fixed Monthly Payment

- Current amount: `$100/month`
- This pays for general support, company development, internal organization, process development/improvement, and support tasks that do not create an immediate sale.
- This fixed monthly payment is separate from event commissions.

### Part 2: Event Commission

- Event commission is earned when a sale becomes valid.
- A sale becomes valid when the client pays a deposit or pays in full.
- Commission is calculated only on the main bar price before tax.
- Add-ons and extras are excluded unless a future special bonus is approved.

## 6. How to Calculate Fernando's Commission

Use these steps for one event:

1. Confirm the sale is valid.
2. Confirm the client paid deposit or full payment.
3. Use only the main bar price before tax.
4. Exclude add-ons and extras.
5. Use the valid sales count for the period to choose the stage.
6. Use the official event price to choose the `<= $430` or `> $430` tier.
7. Multiply by the correct percentage.
8. Round to the nearest whole dollar for simple reference.
9. Add notes when something is unusual.

### Commission Stage Table

| Stage | Valid Sales Count | Events <= $430 | Events > $430 |
| --- | --- | ---: | ---: |
| Stage 1 | 1 to 5 sales | 7% | 8.5% |
| Stage 2 | 6 to 10 sales | 8% | 10% |
| Stage 3 | 11+ sales | 9% | 11.5% |

Sales above 15 stay in Stage 3 for now.

## 7. Valid Sale Rule

- If no deposit or full payment has been received, commission is `$0`.
- The sale becomes valid once the client pays a deposit or pays in full.
- Commission can be paid once the sale is valid, according to the active compensation file.

## 8. Discount and Approval Rules

Fernando cannot:

- Invent discounts or promotions.
- Change prices from the official file.
- Promise exceptions to policy.
- Offer refunds by personal decision.

Approval rules:

- Only the supervisor can approve discounts.
- The supervisor name is still TODO until Jorge confirms it.

## 9. Lead Ownership and Overtake Rule

- The main leader gets the commission.
- If there is a critical delay of 8 hours without client response and risk of losing the sale, the lead can be reassigned/overtaken.
- This is meant to protect the company from losing sales because of lack of follow-up.

## 10. Problems, Cancellations, Chargebacks, and Adjustments

- If the problem is company/system fault, there is no chargeback and the worker does not lose commission.
- If the problem is worker execution/service fault, administration may decide a partial or total chargeback.
- Administrative overpayments and adjustments are applied to future commissions only.
- No immediate repayment is required for adjustments unless Jorge later creates a different approved rule.

## 11. Bako Business Branding Rules

- Bako Business Branding is included as a separate company profile.
- Current payment rules are TBD.
- Do not copy Manna Snack Bars payment rules into Bako unless Jorge specifically approves it.
- Bako may later use hourly pay, project-based pay, commission, salary, bonuses, or mixed pay, but nothing should be invented.

## 12. How to Add a New Worker

1. Copy `knowledge/workers/worker-template.md`.
2. Rename it to the worker's name, lowercase with hyphens.
3. Fill only known information.
4. Leave unknown details as TODO.
5. Copy `knowledge/compensation/compensation-template.md` if the worker needs their own compensation file.
6. Link the worker file to the company file.
7. Link the company file to the worker file.
8. Add the compensation file to `knowledge/compensation/payment-rules-index.md`.
9. Update `knowledge/README.md` or this manual if needed.

## 13. How to Update a Worker's Payment

When changing fixed pay, commission, bonus, or salary:

- Update the worker profile.
- Update the compensation file.
- Update the company profile if it summarizes the amount.
- Update the payment rules index if the status changes.
- Add a note explaining what changed.
- Keep old source notes when helpful.
- Do not change unrelated rules.

Example: if Fernando's fixed monthly payment changes again, update:

- `knowledge/workers/fernando.md`
- `knowledge/compensation/manna-fernando-compensation.md`
- `knowledge/companies/manna-snack-bars.md`
- Any README/manual summary if needed

## 14. How to Update Commission Rules

When changing commission percentages, stages, or pricing:

- Update `manna-fernando-compensation.md`.
- Update `manna-commission-calculator.md`.
- Update `manna-commission-formula.md`.
- Update `manna-commission-examples.md`.
- Update `payment-rules-index.md` if needed.
- Make sure all tables match.
- Do not update only one file and leave the others outdated.

## 15. How to Use This System With ChatGPT or Codex

When asking ChatGPT/Codex to work with this system, tell it to:

- Read the relevant company file first.
- Read the worker file.
- Read the compensation file.
- Read calculator/formula/examples if commission is involved.
- Do not invent missing amounts.
- Use TODO for unknown details.
- Keep Manna and Bako separate.
- Summarize files edited.
- Confirm what was not changed.

Reusable prompt:

> Before editing worker payment rules, read the relevant company profile, worker profile, compensation file, and payment rules index. Only update the specific rule requested. Do not invent missing information. Preserve TODOs where information is unknown. After editing, summarize files changed, amounts changed, rules changed, and rules not changed.

## 16. Required Safety Rules for Future Edits

- Never invent payment amounts.
- Never invent commission percentages.
- Never invent bonus rules.
- Never copy one company's rules into another company unless Jorge approves it.
- Never change old rules silently.
- Always add notes when a payment amount changes.
- Always keep fixed pay separate from commission.
- Always preserve source notes when the old source is different from the current active rule.
- Always update all linked files when a rule appears in more than one place.
- Always leave TODO when something is unknown.

## 17. Missing Information / TODOs

Current missing information:

- Fernando's official role/title
- Exact payment period/date for the `$100/month` fixed payment
- Official supervisor for discount approvals
- Approved bonus rules for Fernando, if any
- Bako Business Branding payment system
- Future worker profiles and rules

## 18. Review Cycle

- Manna/Fernando compensation and rules should be reviewed every 2 months.
- During review, check if fixed pay, commission percentages, bonus rules, worker responsibilities, and approval rules still make sense.

## 19. Quick Reference

### Fernando / Manna

- Fixed monthly payment: `$100/month`
- Event commission: separate
- Valid sale: deposit or full payment received
- Commission base: main bar before tax
- Add-ons/extras: excluded unless special bonus is approved
- Discounts: supervisor approval only
- Review cycle: every 2 months

### Bako

- Payment rules: TBD
- Do not copy Manna rules into Bako without approval

## 20. Last Updated

2026-06-28
