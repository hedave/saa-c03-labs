# Checklist (David runs this by hand)

Agents do not check these boxes. David does.

## Before any lab

- [ ] Still on AWS **Free** plan (not Paid)
- [ ] Credits remaining recorded (not only month-to-date)
- [ ] Budgets exist at $1, $5, and $10
- [ ] Region will be `us-east-1` only
- [ ] Anything created will be tagged `Project=saa-c03` and `AutoDestroy=true`
- [ ] No NAT, no Control Tower, no Organizations join
- [ ] No AWS keys in this repo; no long-lived access keys for agents
- [ ] No `terraform apply` / destroy / AWS create unless I type `ALLOW_APPLY=true`
- [ ] Nothing on the NEVER list unless I type `ALLOW_PAID=true`

## NEVER without `ALLOW_PAID=true`

- [ ] No NAT Gateway
- [ ] No Multi-AZ RDS left running
- [ ] No ALB or NLB left running
- [ ] No EKS
- [ ] No Organizations or Control Tower (joining can auto-upgrade Free plan and void credits)
- [ ] No upgrade to Paid just for Security Hub
- [ ] No overnight `terraform apply`
- [ ] No long-lived AWS access keys for agents

## After the lab, same day

- [ ] EC2 / Lambda / RDS (if used) deleted the same day
- [ ] Leftover checks in `us-east-1` from [DESTROY.md](DESTROY.md)
- [ ] Credits remaining checked again
- [ ] No ALB, NLB, NAT, Multi-AZ RDS, or EKS left running
