# Expectations.md

# Expectations (clear demo checklist)

## 1) What you must demonstrate (live or recorded)
Pick **one** demo mode:

### Option A — Local demo (acceptable)
- `docker compose up` runs all services
- You show the app in browser + backend logs + DB working
- You show CI pipeline running Dev → QA → Stage (Stage can redeploy compose)

### Option B — AWS demo (preferred / bonus)
- Stage environment deployed from pipeline
- Provide a **reachable URL** (DNS/ALB/public endpoint)
- Show pipeline logs proving deploy is automated

## 2) Required pipeline evidence
You must show:
- Dev jobs: lint + unit tests + build + docker image build
- QA jobs: environment starts + integration tests run
- Stage jobs: deployment happens automatically after QA success
- Artifacts: test reports or logs attached to pipeline run

## 3) Secrets expectations (must)
Pick one approach and explain it in `SECURITY.md`:

### Option A — CI variables/secrets (acceptable)
- Use GitLab CI variables / GitHub secrets
- Inject at runtime (not committed)

### Option B — Federated auth (bonus)
- AWS OIDC / short-lived credentials
- Explain why it’s better than long-lived keys

Red flags:
- secrets committed to git
- `.env` with real values committed
- printing secrets in logs

## 4) Docker expectations (must)
- Frontend and backend have Dockerfiles
- Containers run reliably using environment variables
- Compose network wiring works (backend can reach DB)
- Bonus points:
  - multi-stage builds
  - non-root runtime user
  - healthchecks

## 5) Documentation expectations (must)
You must include:
- `AI_USAGE.md`:
  - what AI was used for
  - prompts (high-level is fine)
  - what you changed manually
- `SECURITY.md`:
  - secrets strategy
  - risk notes + mitigations
- `ENHANCEMENT.md`:
  - “next 10 improvements” (security/perf/qa/ops)
  - what you would do in week-1 / month-1

## 6) How we will question you (be ready)
We will ask about:
- “How do you store and inject secrets in CI and runtime?”
- “Artifacts vs cache — why and where?”
- “How do you prevent deploying from feature branches?”
- “How would you roll back Stage?”
- “What fails first in real systems and how would you detect it?”

## 7) What ‘done’ looks like
Done means:
- One command runs locally OR one URL runs on AWS
- CI pipeline clearly promotes Dev → QA → Stage without manual hacks
- You can explain each step confidently
