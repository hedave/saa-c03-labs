# Destroy notes

David tears down by hand in `us-east-1`. Timed labs (EC2, Lambda, RDS) are deleted the same day they are created. Agents do not apply, destroy, or create AWS resources unless the human types `ALLOW_APPLY=true`.

## After every lab, same day

1. Delete the lab’s resources (console or a human-run `terraform destroy` with `ALLOW_APPLY=true`).
2. Confirm tags `Project=saa-c03` and `AutoDestroy=true` were on everything that existed.
3. Walk leftover checks below in **us-east-1** only.
4. Record credits remaining (not only month-to-date) in a note if they moved. See [COST.md](../../COST.md).

## Leftover checks (us-east-1)

Look for anything still billed after the lab:

- EC2 instances, EBS volumes, snapshots, AMIs, Elastic IPs
- Lambda functions and related IAM roles created for the lab
- RDS instances (especially Multi-AZ left running)
- ALB / NLB
- NAT Gateways, unused IGWs, extra VPCs, extra subnets
- EKS clusters
- S3 buckets created for the lab (empty, then delete)
- CloudWatch log groups created for the lab

## NEVER leave running (needs `ALLOW_PAID=true` even to create)

See [README.md](README.md). NAT Gateway, Multi-AZ RDS left running, ALB or NLB left running, and EKS are in that list. If one of these exists without `ALLOW_PAID=true`, stop and destroy it the same day.

## Plan

Do not join Organizations or Control Tower. Do not upgrade to Paid. Those can void Free-plan credits.
