# README.md

# CI/CD Take-Home Assignment (KISS)

## Goal
Show you can build, test, containerize, and promote a small full-stack app through **Dev → QA → Stage** using **CI/CD** (not manual steps).

Timebox: **~4 hours** (use AI if you want; document it).

## Fixed tools (must)
- CI/CD: **GitLab CI/CD** (preferred). If you cannot, use GitHub Actions and explain why.
- Backend: **Java (Maven)** (Spring Boot preferred)
- Frontend: **NodeJS (npm)** (Next.js preferred)
- **Docker**: must (Dockerfiles + runnable)
- Kubernetes: optional (bonus)
- Infra: **AWS OR your laptop** (Docker Compose is the simplest acceptable demo)

## What to build (minimal)
A small app with:
- Frontend calls backend API
- Backend has:
  - `GET /health`
  - `GET /api/items`
  - `POST /api/items`
- Database: PostgreSQL (can be containerized)
- Optional bonus service: Redis or worker

## Required repo output
You must commit:
- `Dockerfile` for frontend + backend (multi-stage recommended)
- `docker-compose.yml` (runs the full stack locally)
- CI pipeline config:
  - `.gitlab-ci.yml` (preferred) or `.github/workflows/*.yml`
- Docs:
  - `AI_USAGE.md` (required if you used AI)
  - `SECURITY.md`
  - `ENHANCEMENT.md`

## CI/CD pipeline requirements
Your pipeline must have **3 phases** and **automatic promotion** when gates pass:

### 1) Dev (auto)
- Lint + unit tests (frontend + backend)
- Build artifacts
- Build Docker images

### 2) QA (auto after Dev success)
- Spin up stack (compose in CI or equivalent)
- Integration tests that hit real endpoints

### 3) Stage (auto after QA success)
Deploy to an environment (pick one):
- Option A (simple): laptop/VM via docker-compose (Stage URL can be local + recorded demo)
- Option B (bonus): AWS (ECS/EKS/EC2) with a reachable URL

## Submission
Provide:
- Repo link (your fork/project)
- Pipeline link showing Dev → QA → Stage green
- Stage URL (or recorded demo if local)
- Short README section: “How to run locally” + “How to trigger pipeline”

## What we will assess
We will scrutinize:
- Your CI/CD design (gates, artifacts, promotion)
- Secrets handling (no secrets in repo)
- Dockerfiles (reproducible builds, runtime config)
- Your ability to explain choices, tradeoffs, and failures

Please read and unederstand more instructions from `Expectations.md`, `Options.md`, and `SCORE.md`.
For any question or clarifitcation reachout Amit Karpe.
