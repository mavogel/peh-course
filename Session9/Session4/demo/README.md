# Session 4 Demo — Day 1 Verification

## Demo Overview
Run all three test suites to verify the integrated platform works end-to-end.

## Dependencies — Run This First
Requires a running Kind cluster with Crossplane and Gatekeeper from Sessions 2-3.

## Steps
```bash
# 1. Cluster health
python3 test-cluster-health.py

# 2. Infrastructure (Crossplane resources)
python3 test-infrastructure.py

# 3. Policies (Gatekeeper constraints active)
python3 test-policies.py
```

## Key Concepts
- Three test suites validate the three pillars: runtime, infra, policy
- In production, these run in CI as platform smoke tests
- If any fail, you know exactly which layer has a problem
