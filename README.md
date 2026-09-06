# Jacob Greenberg

Full-stack engineer building production healthcare and AI-agent systems.
Fourteen years inside medical billing and revenue cycle (since 2012); writing
the software for it since 2014. VP of Technology and co-owner at
[ClaimCarePro](https://claimcarepro.com), where I'm the sole engineer on the
platform the business runs on.

**Stack:** TypeScript · React 19 / Next.js 15 · AWS (Amplify Gen 2, AppSync,
Lambda, DynamoDB, Bedrock) · Python · Claude / agent orchestration · 837P/835
EDI · HIPAA-constrained AI

## What I've built

### ClaimCarePro — multi-tenant EHR & billing platform (private: HIPAA)

Sole engineer on a production platform serving 21 practice organizations,
39 providers, 2,484 patients, and 32,759 live charge lines.
~298k lines of TypeScript, 2,937 tests across 188 suites, 67 data models,
172 API routes, 23 AppSync resolvers, 9 Lambdas.

- Multimodal Claude on Bedrock reads scanned and handwritten CMS-1500
  superbills into structured claims with per-field confidence (PHI stays
  under BAA).
- 837P/835 EDI, 270/271 eligibility, MUE + CCI/NCCI claim scrubbing.
- Immutable financial ledger: integer cents, idempotency keys.
- Resolver-layer tenant isolation, 11+ RBAC roles, break-the-glass access.
- CI gate that fails the build if marketing copy makes an unsubstantiated
  claim.

### claude-master-control — agent orchestration control plane (public)

Local-first control plane for parallel Claude Code sessions across 37
projects: 40-command CLI, 25-route API, React dashboard over one SQLite
store with a single enforced write path. 1,357 recorded headless agent
runs over 26 consecutive days. Four-tier agent permission model asserted
in the test suite — no headless agent can hold a tool that mutates an
external system.

### MLS listing platform (private: commercial)

Broker SaaS that validates listings, maps them to RESO Data Dictionary 2.0
with Claude on Bedrock, and submits to the MLS. 61k lines, 1,739 tests,
18 Lambdas — plus a 14.7k-line browser extension with a resumable form
walker that survives full page navigations on a legacy JSP form.

## Why most of this is private

The EHR platform handles PHI and stays private under HIPAA. The MLS
platform is a commercial product. Where I can't show source, I show
architecture: engineering-notes has deep writeups with real production
numbers.

A note on commit dates: my public repos were extracted or released in
2026, so their visible history starts there. The work predates it — this
account dates to 2016, and the archived jhipster-billing-application
(2018) is an early public pass at the billing-software problem I've been
working on since 2012.

## Contact

Tampa Bay, FL · remote (US) ·
[LinkedIn](https://linkedin.com/in/jacob-greenberg-fl) ·
jacob.greenberg45@gmail.com
