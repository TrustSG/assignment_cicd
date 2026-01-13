# SCORE.md

# Scoring (100 points + bonuses)

We score what you **commit + automate + can explain**.
We also consider your **Issues/PRs/branches** as part of your engineering process.

## 10 categories × 10 points = 100

1) Documentation quality (10)
- Clear README, run steps, pipeline overview

2) Repo workflow hygiene (10)
- Issue → branch → PR/MR → review notes → merge
- Small commits, meaningful messages

3) CI pipeline structure (10)
- Clear Dev/QA/Stage stages with gates and promotion

4) Build correctness (10)
- Maven + npm builds deterministic, no “works on my machine”

5) Test depth (10)
- Unit tests + at least one integration/smoke test in QA

6) Containerization (10)
- Dockerfiles + compose wiring + repeatable runtime config

7) Secrets handling (10)
- No secrets in repo, correct injection, good explanation

8) Deployment automation (10)
- Stage deploy from pipeline (not manual)
- Output includes URL or demo proof

9) Quality signals (10)
- Reports/artifacts, logs readable, failure modes handled

10) Engineering judgement (10)
- `SECURITY.md` + `ENHANCEMENT.md` show realistic next steps,
  tradeoffs, and what you’d do with more time

## Bonus points (extra)
- +10 Kubernetes / EKS / OpenShift deployment working end-to-end
- +10 GitOps / K8s-native pipelines (ArgoCD / FluxCD / Tekton) working

## Notes
- AI use is allowed and not penalized **if** documented in `AI_USAGE.md`
- If you cannot explain your own pipeline, we will score down even if it “works”
