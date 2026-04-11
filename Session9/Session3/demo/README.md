# Session 3 Demo — Self-Service IaC + Shift-Left Policies + AI Templates

## Demo Overview
Submit a self-service database claim, catch policy violations with conftest,
and explore AI-generated service configuration.

## Dependencies — Run This First
Requires a running Kind cluster with Crossplane installed (from Session 2):
```bash
helm repo add crossplane-stable https://charts.crossplane.io/stable
helm install crossplane crossplane-stable/crossplane --namespace crossplane-system --create-namespace
```

## Steps
```bash
# 1. Review the Crossplane XRD (the "menu" developers see)
cat xrd-postgresql.yaml

# 2. Review the Composition (what the platform team wrote behind the scenes)
cat composition-postgresql.yaml

# 3. Submit a database claim (the developer experience)
cat demo-app-database.yaml
kubectl apply -f demo-app-database.yaml

# 4. Run conftest to catch a bad manifest
conftest test conftest-tests/test-manifests.yaml -p conftest-tests/

# 5. Review the Rego policy that caught it
cat conftest-tests/policy.rego

# 6. AI-POWERED: Review the AI-generated service template
cat backstage-ai-template.yaml
# AI generates boilerplate k8s config from a natural language description
```

## Key Concepts
- Developer submits 10 lines of YAML, platform provisions the database
- conftest catches violations BEFORE code reaches the cluster
- AI templates: developers describe their service in plain English, AI generates the Kubernetes config
- The platform validates AI-generated output with the same policies as human-written code
