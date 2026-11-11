# Spring Winter

Deploy apps and agents into an AWS account you own.

[springwinter.dev](https://springwinter.dev) · [Docs](https://docs.springwinter.dev) · [Create an account](https://springwinter.dev/auth?mode=signup)

Spring Winter is a hosted control plane. It creates and updates web servers, workers, static sites, databases, caches, storage, and branch previews in the AWS account you connect. The workloads stay in that account. You choose the role permissions.

## What you can deploy

| Resource | What it is |
| --- | --- |
| Web servers | An app from GitHub or a container image |
| Workers | Background jobs with no public URL |
| Static websites | A site built from GitHub, served with S3 and CloudFront |
| SQL databases | PostgreSQL or MySQL on Aurora or RDS |
| Caches | A private Valkey cache over TLS |
| Storage | Private S3 buckets |
| Previews | A code branch at its own URL |

## How a deploy works

1. **Choose a resource.** Web server, worker, static website, database, cache, or storage bucket.
2. **Connect and set up.** Pick a GitHub repository or container image. Set the size and environment variables.
3. **Deploy.** Spring Winter checks AWS access, builds the app when needed, and deploys the resource in your account.

Connect AWS by launching a CloudFormation stack in your account. The stack creates a role with a unique external ID. Connect GitHub so builds and deploys can run from your repositories.

## For agents

Give an agent the Spring Winter skill. It covers how to choose a resource, review cost and impact, and confirm that AWS changes are complete. Copy it into `.agents/skills/springwinter/SKILL.md` from [springwinter.dev](https://springwinter.dev).

## Docs

- [Quickstart](https://docs.springwinter.dev/quickstart)
- [Connect AWS](https://docs.springwinter.dev/connect-aws)
- [Connect GitHub](https://docs.springwinter.dev/connect-github)
- [API reference](https://docs.springwinter.dev/api-reference/overview)
