# Session 7 Demo — Chaos Engineering, Progressive Delivery + AI Runbooks

## Demo Overview
Inject network latency with Chaos Mesh, deploy a canary with automated rollback,
and try AI-powered runbook automation.

## Dependencies — Run This First
Requires a running Kind cluster (from Session 2) with Chaos Mesh installed:
```bash
helm repo add chaos-mesh https://charts.chaos-mesh.org
helm install chaos-mesh chaos-mesh/chaos-mesh --namespace chaos-mesh --create-namespace
```

## Steps
```bash
# 1. Review the chaos experiment definition
cat chaos-network-delay.yaml

# 2. Apply it (adds 100ms latency to api-service pods)
kubectl apply -f chaos-network-delay.yaml

# 3. Run the chaos orchestrator to monitor
python3 chaos-runner.py

# 4. Deploy a canary
kubectl apply -f canary-deployment.yaml

# 5. Run the automated rollback controller
python3 rollback-controller.py

# 6. AI-POWERED: Convert a markdown runbook to executable steps
python3 runbook-automator.py
# Parses runbook → diagnostic steps → action steps → approval gates
# AI adds safety checks automatically
```

## Key Concepts
- Chaos experiments discover how your system breaks before users do
- Canary + rollback controller = automated safe deployments
- AI runbook automation takes your existing markdown runbooks and makes them executable
- Safety built in: AI identifies which steps need human approval vs. auto-execute
- This is NOT replacing SREs — it's giving them a co-pilot
