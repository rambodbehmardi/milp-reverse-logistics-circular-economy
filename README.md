# Multi-Objective MILP for Sustainable Reverse Logistics
### Closed-Loop Supply Chain Design under Disruption and Return Uncertainty

**Status:** Manuscript under review · 2026  
**Domain:** Mathematical Optimisation · Circular Economy · Supply Chain Resilience

---

## Research Problem

How can a multi-echelon manufacturing supply chain simultaneously optimise 
economic performance, environmental impact, and social outcomes while 
embedding circular economy principles under real-world disruption and 
return-rate uncertainty?

## Framework

**Phase I — Stochastic Multi-Objective MILP**

A multi-product, multi-period mixed-integer linear programming model formulated 
for a closed-loop network comprising suppliers, primary and secondary 
manufacturers, warehouses, inspection centres, recycling centres, and disposal 
centres. Three objectives are simultaneously optimised:

- **Economic:** Maximise total profit across forward and reverse flows
- **Environmental:** Minimise chemical use, energy consumption, and emissions
- **Social:** Maximise employment creation and domestic technology development

Disruption uncertainty is modelled via three scenario-based sanction levels. 
Resilience strategies (capacity expansion, facility reinforcement, direct 
routing, safety stock) are embedded as endogenous decision variables.

**Phase II — Sensitivity and Scenario Analysis**

- Pareto frontier generation via the epsilon-constraint method
- Return rate impact on recycling, repair, and waste reduction volumes
- Comparative resilience strategy analysis across disruption scenarios
- Contour and ridge visualisation of circular economy performance

## Supplier Screening: Hybrid DEA + PCA

A two-stage screening procedure precedes network optimisation:

1. **DEA (CCR model):** Efficiency scores computed for 15 candidate suppliers 
   (range: 0.428–1.000); five suppliers selected above the 0.75 threshold
2. **PCA:** Multicollinearity among evaluation criteria reduced before 
   efficiency scoring to improve robustness

## Key Findings

- Product return rates are the dominant driver of circular economy performance; 
  a 20% increase drives substantial growth in recycling and repair volumes
- Capacity expansion yields the strongest network resilience under severe disruption
- Secondary manufacturer disruptions impose the greatest supply shortfall — 
  larger than supplier or warehouse failures combined
- Social and environmental improvements are achievable but at higher cost, 
  creating measurable Pareto trade-offs with profit

## Implementation
```
Language : Python  
Solvers  : OR-Tools · PuLP  
Analysis : NumPy · Pandas · Matplotlib  
Visuals  : Contour plots · Pareto frontier · Ridge density plots
```

## Repository Structure
```
src/
  dea_pca_supplier_screening.py   # Hybrid DEA+PCA evaluation
  milp_model.py                   # Stochastic MILP formulation
  epsilon_constraint.py           # Pareto generation procedure
  sensitivity_analysis.py         # Scenario and return-rate analysis
  visualisation.py                # Contour, ridge, and Pareto plots
data/
  supplier_criteria.csv           # Input data for DEA screening
results/
  pareto_solutions.csv            # Non-dominated solution set
```

## Citation

Behmardi Kalantari, R. (2026). *A Multi-Objective Optimisation Framework 
for Sustainable Reverse Logistics and Circular Economy under Disruption 
and Return Uncertainty.* Manuscript under review.
