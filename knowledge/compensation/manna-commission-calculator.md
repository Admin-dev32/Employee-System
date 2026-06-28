# Manna Snack Bars — Fernando Commission Calculator Reference

## Purpose

This is a simple human-readable reference for calculating Fernando's commission for one Manna Snack Bars event.

This is not an app, database, admin panel, or automated payroll system. It is an internal knowledge reference that can be edited manually.

## Inputs

Use these inputs for each event:

| Input | Meaning |
| --- | --- |
| `main_bar_price_before_tax` | The main bar price before tax. This is the amount used for commission. |
| `official_event_price` | The official client-facing event price. This is used to decide whether the event is `<= $430` or `> $430`. |
| `monthly_sales_count` | Number of valid sales in the period. This decides the commission stage. |
| `is_valid_sale` | `Yes` only when the client has paid a deposit or paid in full. |
| `has_supervisor_discount_approval` | `Yes` only if the supervisor approved any discount. |
| `notes` | Any important context about the sale, discount approval, or calculation. |

## Valid Sale Rule

If the sale is not valid, commission is `$0`.

A sale becomes valid once the client pays a deposit or pays in full.

## Commission Base Rule

Commission is calculated only on `main_bar_price_before_tax`.

Add-ons and extras are excluded from standard commission.

## Stage Rule

Stage is based on the number of valid sales in the period:

| Monthly Valid Sales Count | Stage |
| --- | --- |
| 1 to 5 sales | Stage 1 |
| 6 to 10 sales | Stage 2 |
| 11+ sales | Stage 3 |

## Percentage Rule

| Stage | Events <= $430 | Events > $430 |
| --- | --- | --- |
| Stage 1 | 7% | 8.5% |
| Stage 2 | 8% | 10% |
| Stage 3 | 9% | 11.5% |

## Simple Calculation Steps

1. Confirm `is_valid_sale`.
   - If no deposit or full payment has been received, commission is `$0`.
2. Confirm the sale uses an authorized official price.
   - If there was a discount, confirm `has_supervisor_discount_approval`.
3. Use `monthly_sales_count` to choose the stage.
4. Use `official_event_price` to choose the event price tier:
   - `<= $430`
   - `> $430`
5. Multiply `main_bar_price_before_tax` by the correct percentage.
6. Round the result to the nearest whole dollar for simple reference reporting.
7. Add any important context in `notes`.

## Manual Formula

```text
if is_valid_sale is not Yes:
  commission = $0
else:
  stage = stage based on monthly_sales_count
  percentage = percentage for stage and official_event_price tier
  commission = main_bar_price_before_tax × percentage
  rounded_commission = rounded commission amount
```

## Important Notes

- Numbers in reference examples are rounded.
- If official pricing changes, the example table must be updated.
- Keep this file easy to edit manually.
- Do not include add-ons or extras in the standard commission calculation.
- Do not add future bonus systems here unless specifically approved.

## TODO: Future Add-On Bonuses

TODO: Add future add-on bonus rules only if they are specifically approved.

## Last Updated

2026-06-28
