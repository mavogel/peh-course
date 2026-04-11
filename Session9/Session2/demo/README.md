# Session 2 Demo — Control Plane Walkthrough

## Demo Overview
Provision a Kind cluster and create isolated team namespaces with quotas and RBAC.

## Dependencies — Run This First
```bash
kind create cluster --name workshop
pip3 install pulumi pulumi-kubernetes --break-system-packages
```

## Steps
```bash
# 1. Review the Pulumi cluster code
cat pulumi-cluster/__main__.py

# 2. Provision a team namespace with quotas
python3 namespace-provisioner.py --namespace team-alpha --env dev --team alpha

# 3. Provision a second namespace
python3 namespace-provisioner.py --namespace team-beta --env dev --team beta

# 4. Verify what was created
kubectl get ns
kubectl describe resourcequota -n team-alpha

# 5. Apply platform admin RBAC
kubectl apply -f rbac-platform-admin.yaml

# 6. Review the platform services that run in the control plane
cat platform-services.yaml
```

## Key Concepts
- One command creates namespace + quota + limit range + RBAC
- Developers never touch cluster-level resources
- Resource quotas prevent any team from starving others
