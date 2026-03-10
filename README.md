# cancer-metabolic-adaptive-state-space
A simulation-driven systems oncology framework that models cancer as a dynamic metabolic-adaptive landscape linking bioenergetics, DNA repair, phenotypic plasticity, and therapy-driven state transitions.

## Cancer as a Metabolic-Adaptive State Space

A simulation-based systems oncology project that models cancer as a **dynamic metabolic-adaptive landscape** rather than a static mutation-defined disease class.

This repository provides a proof-of-concept framework in which tumour cells occupy and transition between biologically interpretable states shaped by:

- glycolysis and lactate production,
- oxidative metabolism,
- glutamine dependence,
- redox balance,
- DNA repair capacity,
- replication and oxidative stress,
- epithelial-mesenchymal plasticity,
- stemness,
- drug tolerance,
- mitochondrial health.

The project uses **simulated datasets benchmarked to literature-supported qualitative patterns** and applies machine learning, unsupervised learning, and transition analysis to test the hypothesis that cancer can be represented as a **metabolic-adaptive state space**.

## Project concept

Most cancer models classify tumours by mutations, histology, or molecular subtype. This project explores a different idea:

> cancer may be better understood as a dynamic system that moves through adaptive states under environmental and therapeutic stress.

In this framework, tumour populations do not simply “belong” to one fixed identity. Instead, they may shift between states such as:

- **Glycolytic Proliferative**
- **OXPHOS Competent**
- **Glutamine Addicted**
- **Hybrid Plastic**
- **Repair-Deficient Stressed**
- **Drug-Tolerant Adaptive**

The repository asks whether the **structure of these states** and the **routes between them** can reveal vulnerabilities that static class labels miss.

## Repository contents

```text
.
├── README.md
├── MODELCARD.md
├── DATASHEET.md
├── cancer_state_space_simulation.py
├── cancer_state_space_simulation_notebook.ipynb
└── cancer_state_space_outputs/
    ├── simulated_cancer_state_space_cross_sectional.csv
    ├── simulated_cancer_state_space_longitudinal.csv
    ├── state_summary_means.csv
    ├── stressor_summary_means.csv
    ├── classification_results.csv
    ├── regression_results.csv
    ├── classifier_feature_importance.csv
    ├── regressor_feature_importance.csv
    ├── transition_matrix_therapy.csv
    ├── transition_matrix_nutrient.csv
    ├── transition_matrix_hypoxia.csv
    ├── transition_matrix_genotoxic.csv
    ├── transition_bottleneck_scores.csv
    ├── summary_results.csv
    └── figures/
```
## What the code does
The main script:
- 1.	Simulates cross-sectional tumour-state data
- 2.	Simulates longitudinal state transitions under stress
- 3.	Builds supervised ML models to classify tumour state
- 4.	Builds regression models to predict drug tolerance
- 5.	Uses unsupervised learning to assess latent landscape structure
- 6.	Calculates stress-driven transition matrices
- 7.	Identifies adaptive bottlenecks, especially under therapy pressure
- 8.	Generates figures and exportable result tables

## Simulated biological dimensions
The simulation includes the following variables:
	•	glucose uptake
	•	lactate secretion
	•	OCR
	•	ECAR
	•	glutamine uptake
	•	LDHA expression
	•	GLS expression
	•	redox ratio
	•	ROS stress
	•	ATP pool
	•	DNA repair capacity
	•	replication stress
	•	hypoxia response
	•	EMT plasticity
	•	stemness
	•	proliferation
	•	drug tolerance
	•	mitochondrial health
	•	derived vulnerability score

These variables are used to construct a state space spanning metabolism, stress adaptation, genome maintenance, and phenotypic plasticity.

## Stress conditions modeled
The framework models tumour adaptation under:
	•	Baseline
	•	Nutrient Stress
	•	Hypoxia-like Stress
	•	Genotoxic Stress
	•	Therapy Pressure

These perturbations allow the project to simulate movement through state space, not only static state assignment.

## Key outputs
Typical outputs include:
	•	latent-space visualizations of tumour states
	•	classifier and regressor performance tables
	•	confusion matrices
	•	feature-importance rankings
	•	therapy-pressure transition matrices
	•	bottleneck ranking of adaptive states
	•	summary statistics by state and by stress condition

## Main findings 
In the current simulation:
	•	tumour states are highly separable in latent space,
	•	machine-learning models classify states with very high performance,
	•	drug tolerance is predictable from integrated metabolic-adaptive features,
	•	therapy pressure drives transitions toward a Drug-Tolerant Adaptive state,
	•	adaptive bottlenecks can be identified from transition structure.

This supports the central idea that cancer may be interpreted as a state-transition problem.
Important limitations

## This repository is a simulation-based proof of concept.
	•	The datasets are simulated
	•	Values are not patient measurements
	•	Numerical ranges are not clinical reference values
	•	The simulation is literature-anchored qualitatively, not empirically fitted to one cohort
	•	Results should be interpreted as conceptual and methodological demonstrations

This project is intended to show that a metabolic-adaptive state-space framework is biologically interpretable and computationally tractable.

## Intended use
This repository is suitable for:
	•	concept demonstration
	•	methods development
	•	teaching systems oncology
	•	hypothesis generation
	•	grant or manuscript prototyping
	•	future extension to real multi-omics datasets

It is not intended for direct clinical decision-making.

## Future directions
Possible next steps include:
	•	fitting the framework to real tumour multi-omics data
	•	integrating spatial transcriptomics or metabolomics
	•	modeling immune-microenvironment interactions
	•	adding lipid metabolism and one-carbon metabolism
	•	validating transition bottlenecks experimentally
	•	testing whether transition-based vulnerabilities outperform state-only targeting

## Citation
**Petalcorin, M.I.R.** (2026). Cancer as a Metabolic-Adaptive State Space: A Systems Framework Linking Bioenergetics, Genome Maintenance, and Phenotypic Plasticity. https://github.com/mpetalcorin/cancer-metabolic-adaptive-state-space
