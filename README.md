# SAA-C03 labs

David Hernandez studying [AWS Certified Solutions Architect – Associate (SAA-C03)](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.html) in public. The study is the portfolio.

I am using agentic AI to learn AWS the way an architect works, and I publish the corrections. I do not pretend to be an expert yet.

This is SAA-C03. Not a later exam.

## Exam (official)

| | |
|---|---|
| Exam | AWS Certified Solutions Architect – Associate (SAA-C03) |
| Questions | 65 |
| Time | 130 minutes |
| Passing score | 720 |

### Domains

| Domain | Weight |
|---|---|
| Design Secure Architectures | 30% |
| Design Resilient Architectures | 26% |
| Design High-Performing Architectures | 24% |
| Design Cost-Optimized Architectures | 20% |

Source: the [official SAA-C03 exam guide](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.html) only, plus [AWS service documentation](https://docs.aws.amazon.com/), [service FAQs](https://aws.amazon.com/faqs/), and the [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html).

No commercial books.

## Loop

1. **See** — official sources (exam guide, service docs, FAQs, Well-Architected).
2. **Do** — labs in this repo.
3. **Teach** — X receipts. This repo is the proof.

## Cost

AWS Free plan. Region `us-east-1` only. Tags on anything created: `Project=saa-c03`, `AutoDestroy=true`.

Details and credit snapshot: [COST.md](COST.md).

## Week 00

Guardrails before labs: [weeks/00-guardrails/](weeks/00-guardrails/). Destroy notes and a checklist David runs by hand.

Agents in this repo may draft Terraform or CDK and run `terraform plan`. They may not `terraform apply`, destroy, or create AWS resources unless a human types `ALLOW_APPLY=true`.
