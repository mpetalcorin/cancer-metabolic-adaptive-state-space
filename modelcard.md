# Model Card

## Model name

Cancer as a Metabolic-Adaptive State Space


## Model type

This repository contains a **simulation-driven systems framework** plus multiple machine-learning models, including:

- multiclass classifiers for tumour-state prediction
- regression models for drug-tolerance prediction
- unsupervised clustering and latent-space models
- transition and bottleneck analyses over simulated longitudinal state trajectories

The project should be treated as a **research prototype**, not a deployed production model.


## Intended purpose

The purpose of the framework is to test the hypothesis that cancer is better represented as a **dynamic adaptive landscape** than as a static class label. The model is intended to:

- classify simulated tumour samples into adaptive metabolic states
- predict adaptive drug tolerance from integrated metabolic and stress features
- identify state-transition bottlenecks under stress
- support systems-level reasoning about metabolism, DNA repair, and phenotypic plasticity


## Intended users

This repository is intended for:

- computational biologists
- cancer metabolism researchers
- systems biologists
- machine-learning researchers in biomedicine
- students learning simulation-based modelling
- investigators developing grant or manuscript concepts


## Out-of-scope use

This framework is **not intended** for:

- clinical diagnosis
- treatment recommendation
- patient risk scoring
- biomarker reporting for medical use
- direct translation to human decision-making without extensive validation


## Training and input data

The models were trained on **simulated datasets** generated from literature-anchored qualitative assumptions.

The simulated feature set includes:

- glucose uptake
- lactate secretion
- OCR
- ECAR
- glutamine uptake
- LDHA expression
- GLS expression
- redox ratio
- ROS stress
- ATP pool
- DNA repair capacity
- replication stress
- hypoxia response
- EMT plasticity
- stemness
- proliferation
- drug tolerance
- mitochondrial health

A derived vulnerability score is also computed.


## Output labels

### Classification output
The classifier predicts one of the following adaptive states:

- Glycolytic_Proliferative
- OXPHOS_Competent
- Glutamine_Addicted
- Hybrid_Plastic
- Repair_Deficient_Stressed
- Drug_Tolerant_Adaptive

### Regression output
The regression model predicts:

- continuous **drug_tolerance**

### Transition outputs
Transition modules produce:

- stress-specific state-transition matrices
- bottleneck scores
- self-retention metrics
- transition probabilities toward adaptive survival states


## Performance

In the current proof-of-concept run:

- Best classifier: **Logistic Regression**
- Balanced accuracy: **0.996**
- Best regressor: **Random Forest Regressor**
- Drug-tolerance R<sup>2</sup>: **0.825**
- Clustering ARI: **0.967**
- Clustering NMI: **0.965**

These results were obtained on simulated data and should not be interpreted as real-world clinical performance.


## Interpretation

The current results suggest that:

- tumour states are strongly structured in the simulated feature space,
- metabolism, plasticity, and repair-linked stress are major organizers of state identity,
- therapy pressure drives movement toward a drug-tolerant adaptive basin,
- some of the most meaningful vulnerabilities may lie in **state transitions**, not only in states themselves.


## Explainability

The framework uses permutation importance to identify which variables drive prediction.

Top state-classification features in the current run include:

- drug tolerance
- stemness
- glutamine uptake
- EMT plasticity
- GLS expression
- proliferation
- ECAR
- replication stress

This supports interpretability by linking model performance back to biologically meaningful axes.

## Assumptions

This model assumes that:

1. cancer can be represented as a structured adaptive landscape,
2. metabolism, repair, and plasticity co-organize tumour state,
3. state transitions under stress are biologically meaningful,
4. simulated relative patterns capture enough structure for proof-of-concept analysis.


## Limitations

Key limitations include:

- all training data are simulated
- no patient-level calibration is performed
- no real clinical cohort validation is included
- tumour microenvironment complexity is simplified
- immune interactions are not modeled
- spatial heterogeneity is not modeled directly
- lipid metabolism and one-carbon metabolism are not fully represented
- transition probabilities are rule-based, not empirically learned from longitudinal patient data


## Ethical considerations

Because this is a simulation-based research tool, ethical risk is lower than in clinical deployment. However, misuse could occur if users overinterpret simulated outputs as real biological truth.

Users should therefore avoid:

- presenting outputs as patient-derived evidence
- implying medical validity without external validation
- treating simulated rankings as therapeutic recommendations


## Maintenance status

Current status: **research prototype / proof of concept**

Future maintenance may include:

- real-data integration
- external validation
- new features and pathways
- model comparison across tumour contexts
- expanded transition modelling


## Version

Version: 0.1 proof of concept
