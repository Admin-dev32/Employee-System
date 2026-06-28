# Manna Snack Bars — Fernando Commission Formula

## Purpose

This file keeps the Fernando commission logic in a small, plain-language formula format.

It is meant for humans and future AI/Codex sessions to read before editing compensation references.

## Inputs

```text
main_bar_price_before_tax
official_event_price
monthly_sales_count
is_valid_sale
has_supervisor_discount_approval
notes
```

## Formula

```text
If is_valid_sale is No:
  commission = $0

If is_valid_sale is Yes:
  Choose stage from monthly_sales_count:
    1 to 5 valid sales  = Stage 1
    6 to 10 valid sales = Stage 2
    11+ valid sales     = Stage 3

  Choose price tier from official_event_price:
    official_event_price <= $430 = lower tier
    official_event_price > $430  = higher tier

  Choose percentage:
    Stage 1 lower tier = 7%
    Stage 1 higher tier = 8.5%
    Stage 2 lower tier = 8%
    Stage 2 higher tier = 10%
    Stage 3 lower tier = 9%
    Stage 3 higher tier = 11.5%

  commission = main_bar_price_before_tax × percentage
  rounded_commission = commission rounded to the nearest whole dollar
```

## Discount Approval Check

If the event includes a discount, `has_supervisor_discount_approval` must be `Yes`.

This file does not create any new discount rule. It only reflects that discounts require supervisor approval.

## Exclusions

Do not include add-ons or extras in the standard commission formula.

## Pricing Update Reminder

If official pricing changes, update:

- `manna-commission-examples.md`
- Any linked compensation references that include example amounts

## TODO: Future Add-On Bonuses

TODO: Add future add-on bonus formula only if add-on bonuses are specifically approved.

## Last Updated

2026-06-28
