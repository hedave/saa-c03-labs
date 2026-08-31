# Cost

AWS **Free** plan. Not Paid.

Confirmed **2026-08-31**:

| | |
|---|---|
| Credits remaining | $99.99 |
| Month-to-date | $0.00 |
| Credit window ends | 2027-02-26 |

Watch **credits remaining**, not only month-to-date. Month-to-date can read $0.00 while credits are draining.

## Budgets

Create AWS Budgets first, before compute labs:

- $1
- $5
- $10

## Region and tags

- Region: `us-east-1` only.
- Tags on anything created: `Project=saa-c03`, `AutoDestroy=true`.

## Explore AWS $20×5

Order of spend:

1. **Budgets first.**
2. **EC2 / Lambda / RDS** only as timed labs, deleted the same day.
3. **Bedrock** is optional and is not on the SAA-C03 blueprint. Skip it unless a lab explicitly needs it, then delete the same day.

Do not treat Explore AWS credits as permission to leave resources running.

## Plan

Stay on Free. Joining Organizations or Control Tower can auto-upgrade the Free plan and void credits. Do not upgrade to Paid (including “just for Security Hub”) without `ALLOW_PAID=true`. See [weeks/00-guardrails/](weeks/00-guardrails/).
