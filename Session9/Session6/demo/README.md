# Session 6 Demo — Observability, SLOs, Cost + AI Alert Correlation

## Demo Overview
Deploy the OTel collector, review an SLO definition, run cost analysis,
and try AI-powered alert correlation.

## Dependencies — Run This First
Requires a running Kind cluster (from Session 2) with Prometheus installed:
```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install prometheus prometheus-community/kube-prometheus-stack --namespace monitoring --create-namespace
pip3 install pyyaml requests --break-system-packages
```

## Steps
```bash
# 1. Review the OTel collector config (receivers, processors, exporters)
cat otel-collector-config.yaml

# 2. Deploy the collector
kubectl apply -f otel-collector-deployment.yaml

# 3. Review an SLO definition with Sloth
cat sloth-auth-service-slo.yaml

# 4. Run cost analysis
python3 cost-analyzer.py

# 5. AI-POWERED: Correlate noisy alerts into root causes
python3 alert-correlator.py
# 50 raw alerts → grouped into 3 incidents with root cause analysis
```

## Key Concepts
- OTel Collector is the single entry point for all telemetry
- Sloth generates Prometheus recording rules from simple SLO YAML
- Cost visibility is a platform responsibility, not an afterthought
- AI alert correlation reduces alert fatigue by grouping related alerts automatically
- Runs locally with heuristics; optionally add an LLM for advanced pattern recognition
