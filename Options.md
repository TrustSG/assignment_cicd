# Options.md

# Options (pick what you like)

## A) App/code starting points (Java + Node friendly)
- GitLab examples (CI patterns you can adapt): https://gitlab.com/gitlab-examples
- GitHub Actions starter workflows (CI templates): https://github.com/actions/starter-workflows/tree/main/ci
- Knative Serving samples (K8s style deployments): https://github.com/knative/docs/tree/main/code-samples/serving
- AWS “modern CI/CD with GitHub + CodePipeline” (AWS pipeline patterns): https://github.com/aws-samples/modern-cicd-with-github-and-aws-codepipeline

## B) Kubernetes / GitOps / Pipeline examples (optional bonuses)
- Skaffold examples (build+deploy to K8s): https://github.com/GoogleContainerTools/skaffold/tree/main/examples
- Tekton pipeline examples (K8s-native CI): https://github.com/tektoncd/pipeline/tree/main/examples
- FluxCD GitHub Action + examples (GitOps): https://github.com/fluxcd/flux2/tree/main/action
- Argo CD example apps (GitOps): https://github.com/argoproj/argocd-example-apps
- FluxCD example repo: https://github.com/AnaisUrlichs/fluxcd-example
- Kubernetes patterns examples: https://github.com/k8spatterns/examples
- OpenShift examples: https://github.com/openshift-examples

## C) Deployment options (choose one)
- Option A (simple): Docker Compose on laptop/VM
- Option B (bonus): AWS ECS on Fargate
- Option C (bonus): AWS EKS / OpenShift / K8s cluster

## D) Test/security options (choose what you can finish)
- Unit tests: Jest (frontend), JUnit (backend)
- Integration tests: Postman/Newman OR curl-based smoke tests OR Testcontainers
- Dependency checks: `npm audit`, Maven dependency scan
- Container scan (bonus): Trivy or similar
