# Session 9 Demo — Workshop Synthesis, Team Topologies & Next Steps

## Demo Overview
Visualize how your platform mirrors your org structure, establish a KPI baseline,
and measure ongoing platform and AI impact.

## Steps
```bash
# 1. Team topology visualization (Conway's Law in practice)
python3 team-topology-generator.py
# Stream-aligned, platform, enabling, and complicated-subsystem teams
# Visualizes interaction modes: collaboration, X-as-a-Service, facilitating

# 2. Collect platform KPIs
python3 platform-kpi-collector.py
# Deployment frequency, lead time, MTTR, change failure rate

# 3. Measure AI impact (if AI features were adopted)
python3 measure-ai-impact.py
```

## Key Concepts
- Conway's Law: your platform will mirror your org structure — design both intentionally
- Team Topologies: stream-aligned teams consume the platform, platform teams build it, enabling teams bridge the gap
- Measure before you build: you need a baseline to prove value
- DORA metrics are the industry standard for engineering productivity
- Present to leadership in business terms: hours saved, cost reduced
- Re-run at 30/60/90 days to show progress
