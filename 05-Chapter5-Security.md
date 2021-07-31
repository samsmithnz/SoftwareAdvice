# Security (and Governance)

Security should always be first, which is why we've put it in chapter 5, because we all get to it eventually.

## Certificates

Certificates always cause pain, eventually...

## Secrets

Never store secrets in source code. NEVER. Put them in a key vault or GitHub secrets and then inject them into your application at deployment time. Make use of Key Vaults, local user secrets, etc to reduce risk.
