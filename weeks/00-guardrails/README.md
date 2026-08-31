# Week 00 — guardrails

David runs the [checklist](CHECKLIST.md) by hand. Agents do not run it and do not create AWS resources.

[Destroy notes](DESTROY.md) cover same-day teardown and leftover checks in `us-east-1`.

## Plan only

Cloud Agents may draft Terraform or CDK and run `terraform plan`. They may not `terraform apply`, `terraform destroy`, or create AWS resources unless the human types `ALLOW_APPLY=true`.

No AWS keys in this repo. No NAT. No Control Tower.

## NEVER without `ALLOW_PAID=true`

Do not create, enable, join, or leave running:

- NAT Gateway
- Multi-AZ RDS left running
- ALB or NLB left running
- EKS
- Organizations or Control Tower (joining can auto-upgrade the Free plan and void credits)
- upgrading to Paid just for Security Hub
- overnight `terraform apply`
- long-lived AWS access keys for agents

`ALLOW_PAID=true` is typed by the human. Agents do not set it.
