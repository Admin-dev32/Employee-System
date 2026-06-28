# Payment Summary Email Template Manual

## Purpose

This template is used to create reusable worker payment summary emails.

It helps Jorge, future ChatGPT sessions, and Codex prepare clear payment summaries without inventing payment amounts or copying rules between workers or companies.

## What This Template Is

This is an HTML email template for payment summaries, commissions, fixed payments, bonuses, and current agreement summaries.

It is reusable for any worker and any company when filled from the correct active knowledge files.

## What This Template Is Not

This template is not:

- A payroll system
- An accounting system
- A legal HR contract
- A replacement for Jorge's approval

## Required Files to Read Before Generating an Email

Before generating a payment summary email, read:

- `knowledge/SYSTEM-MANUAL.md`
- The relevant company file from `knowledge/companies/`
- The relevant worker file from `knowledge/workers/`
- The relevant compensation file from `knowledge/compensation/`
- Commission calculator/formula/examples only if commission is involved
- `knowledge/compensation/payment-rules-index.md` when needed

## Required Information Before Filling the Template

Confirm this information before filling the HTML template:

- Company name
- Company logo URL
- Worker name
- Payment period label
- Payment period date range
- Payment items or commission rows
- Total commissions, if applicable
- Fixed payment amount, if applicable
- Bonus amount, if applicable
- Total payment
- Current agreement rules from active compensation file
- Sender name
- Footer text

## Placeholder Guide

- `{{company_name}}` — company name shown in image alt text and email context.
- `{{company_logo_url}}` — URL for the company logo image.
- `{{worker_name}}` — worker receiving the payment summary.
- `{{payment_period_label}}` — readable period label, such as a month, week, or date range.
- `{{payment_period_date_range}}` — exact date range for the payment period.
- `{{payment_period_badge}}` — short badge text for the email header.
- `{{payment_summary_title}}` — main email title.
- `{{payment_summary_subtitle}}` — short subtitle after the payment period.
- `{{intro_message}}` — opening explanation of the email.
- `{{appreciation_message}}` — short appreciation or context message.
- `{{review_request_message}}` — message asking the worker to review the summary.
- `{{itemized_payment_section_title}}` — title for the itemized payment/commission section.
- `{{payment_item_rows}}` — HTML rows for itemized payments or commissions.
- `{{commission_total_label}}` — label for the total commissions row.
- `{{total_commissions}}` — total commissions amount, if applicable.
- `{{fixed_payment_label}}` — label for fixed pay, if applicable.
- `{{fixed_payment_amount}}` — fixed payment amount, if applicable.
- `{{bonus_label}}` — label for an approved bonus, if applicable.
- `{{bonus_amount}}` — approved bonus amount, if applicable.
- `{{bonus_note}}` — optional note explaining an approved bonus.
- `{{total_payment}}` — total payment amount for the email.
- `{{agreement_section_label}}` — small label for the current agreement section.
- `{{agreement_section_title}}` — title for the current agreement section.
- `{{agreement_summary_rows}}` — HTML rows pulled from the active worker compensation file.
- `{{commission_reference_title}}` — title for the commission reference section.
- `{{commission_stage_header}}` — table header for commission stage names.
- `{{commission_sales_header}}` — table header for sales counts or stage criteria.
- `{{commission_tier_one_header}}` — table header for the first commission tier.
- `{{commission_tier_two_header}}` — table header for the second commission tier.
- `{{commission_reference_rows}}` — HTML rows for commission stages/rates pulled from active compensation/calculator/formula files.
- `{{closing_message}}` — closing note before the sender signature.
- `{{sender_name}}` — name of the sender.
- `{{footer_text}}` — footer text for the email.

## Optional Sections

Remove sections that do not apply to the worker or payment period.

- Commission/payment item table: remove if the worker has no event commissions or itemized payment rows.
- Fixed payment row: remove if the active compensation file does not include fixed pay.
- Bonus row: remove if there is no approved bonus.
- Bonus note: remove if there is no approved bonus note.
- Current agreement section: remove if no agreement summary is needed.
- Commission reference section: remove if the worker does not have commission stages or commission rates.

## Safety Rules

- Never invent payment amounts.
- Never invent commission percentages.
- Never invent bonus rules.
- Never copy Fernando's rules into another worker.
- Never copy Manna rules into Bako unless Jorge approves it.
- Always use the active worker compensation file for current agreement details.
- If information is missing, use TODO or ask Jorge.
- Keep fixed pay separate from commissions.
- Keep bonuses separate from fixed pay and commissions.
- Keep the email mobile-friendly.
- Keep all current contract/agreement details updated from the knowledge system.

## Example Workflow for Fernando

1. Read `knowledge/SYSTEM-MANUAL.md`.
2. Read the Manna company file.
3. Read Fernando's worker file.
4. Read the Manna/Fernando compensation file.
5. Read commission calculator/formula/examples if commission is included.
6. Fill the template using Fernando's current active rules.
7. Confirm the `$100/month` fixed payment is separate from event commissions.
8. Confirm commission percentages were pulled from the active compensation files.
9. Confirm any bonus is approved before adding it.

## Example Workflow for a Future Worker

1. Read that worker's profile.
2. Read that worker's active compensation file.
3. Use only that worker's approved payment rules.
4. Remove sections that do not apply.
5. Do not reuse Fernando-specific amounts or rules.

## Last Updated

2026-06-28
