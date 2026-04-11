# Session 9 Takehome — Your 30/60/90 Day Plan

## Immediate Actions (This Week)

### 1. Map Your Team Topology (20 min)
```bash
python3 ../demo/team-topology-generator.py
```
Identify your stream-aligned, platform, enabling, and complicated-subsystem teams.
Document the interaction modes between them. Does your platform structure
match your org structure? Where are the mismatches?

### 2. Re-Run the Maturity Assessment (10 min)
```bash
python3 platform-maturity-assessment.py
```
Compare with your Day 1 score. Has your understanding changed?

### 3. Establish Cost Baseline (15 min)
```bash
python3 cost-analyzer.py
```

### 4. Document Friction Points (15 min)
```bash
python3 friction-analyzer.py --workflow onboarding
```

## Your 30/60/90 Day Roadmap

### 30 Days
- [ ] Identify top 3 friction points
- [ ] Map your team topology and interaction modes
- [ ] Pick ONE golden path to build first
- [ ] Set up Kind cluster for experimentation
- [ ] Deploy basic namespace provisioner
- [ ] Establish KPI baseline

### 60 Days
- [ ] Build first Backstage software template
- [ ] Implement one Crossplane XRD for self-service
- [ ] Add conftest to CI pipeline
- [ ] Deploy HPA for most variable service
- [ ] Define first SLO
- [ ] Pilot AI doc search (RAG) for your platform docs

### 90 Days
- [ ] Onboard second team to the platform
- [ ] Run first chaos experiment
- [ ] Measure adoption rate and developer satisfaction
- [ ] Evaluate AI alert correlation for your on-call workflow
- [ ] Present results to leadership
- [ ] Plan next quarter's platform roadmap

## Resources
- Book: [The Platform Engineer's Handbook](https://peh-packt.platformetrics.com/) (Packt, 2026)
- Book Code: [github.com/achankra/peh](https://github.com/achankra/peh)
- Platform Engineering community: platformengineering.org
- CNCF Platform WG: tag-app-delivery.cncf.io
