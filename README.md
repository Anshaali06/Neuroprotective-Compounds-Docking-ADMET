# Neuroprotective-Compounds-Docking-ADMET
An in-silico molecular docking and ADMET analysis study evaluating the binding affinity of six neuroprotective compounds against a pesticide-induced neurotoxicity target protein (PDB ID: 4EY7).
## Project Overview
This project focuses on the computational screening of six neuroprotective compounds (DHA, EPA, Curcumin, Resveratrol, Quercetin, and EGCG) against Acetylcholinesterase (AChE), a key enzyme associated with neurotoxicity and neurodegenerative disorders.
Molecular docking was performed using AutoDock Vina to evaluate the binding affinity of the selected compounds toward the target protein. The docking results were further supported by ADMET analysis to assess drug-likeness and pharmacokinetic properties. Protein–ligand interactions of Quercetin, the selected lead compound based on docking and ADMET analysis, were visualized using PyMOL.
Comparative analysis identified EGCG as the strongest binder, followed by Quercetin and Curcumin. However, Quercetin demonstrated the most balanced profile when both docking performance and pharmacokinetic properties were considered.
To identify potential natural inhibitors of Acetylcholinesterase (AChE) through molecular docking and pharmacokinetic analysis.
## Materials
### Target Protein

* PDB ID: 4EY7
* Source: Protein Data Bank (PDB)

### Ligands

The following nutraceutical compounds were selected:

* Quercetin
* Curcumin
* EGCG (Epigallocatechin Gallate)
* Resveratrol
* DHA (Docosahexaenoic Acid)
* EPA (Eicosapentaenoic Acid)



## Methodology

### 1. Protein Preparation
* The crystal structure of Acetylcholinesterase (PDB ID: 4EY7) was downloaded from the Protein Data Bank.
* Water molecules and unwanted heteroatoms were removed.
* Polar hydrogen atoms were added using AutoDock Tools.
*  Gasteiger charges were assigned to the receptor.
* The prepared receptor was saved in PDBQT format for docking studies.

### 2. Ligand Preparation

*  The chemical structures of DHA, EPA, Curcumin, Resveratrol, Quercetin, and EGCG were retrieved from the PubChem database in SDF format.
* The SDF files were converted to PDB format using Open Babel.
* The PDB structures were imported into AutoDock Tools (ADT).
* Hydrogen atoms were added and Gasteiger charges were assigned.
* Rotatable bonds were defined for each ligand.
* The prepared ligands were saved in PDBQT format for molecular docking studies.
### 3. Grid Box Generation

* Binding site coordinates were determined from the co-crystallized ligand.

Grid Center:

* X = -1.624
* Y = -50.091
* Z = 2.056

Grid Dimensions:

* X = 40 Å
* Y = 40 Å
* Z = 40 Å

### 4. Molecular Docking

Software:

* AutoDock Vina v1.2.4

Parameters:

* Exhaustiveness = 8
* Number of Modes = 9

### 5. ADMET Analysis

Top-performing compounds were analyzed using SwissADME for:

* Gastrointestinal absorption
* Lipinski rule compliance
* Bioavailability
* Drug-likeness
* Pharmacokinetic properties



## Docking Results

| Compound    | Binding Affinity (kcal/mol) |
| ----------- | --------------------------- |
| EGCG        | -9.258                      |
| Quercetin   | -8.978                      |
| Curcumin    | -8.806                      |
| Resveratrol | -7.321                      |
| DHA         | -6.415                      |
| EPA         | -6.117                      |



## ADMET Analysis

| Parameter             | EGCG | Quercetin | Curcumin |
| --------------------- | ---- | --------- | -------- |
| GI Absorption         | Low  | High      | High     |
| BBB Permeability      | No   | No        | No       |
| P-gp Substrate        | Yes  | No        | No       |
| Lipinski Violations   | 2    | 0         | 0        |
| Bioavailability Score | 0.17 | 0.55      | 0.55     |

## Result Interpretation

EGCG exhibited the strongest binding affinity toward AChE (-9.258 kcal/mol). However, ADMET analysis revealed limitations including low gastrointestinal absorption and two Lipinski rule violations.
Quercetin demonstrated a strong binding affinity (-8.978 kcal/mol) together with favorable pharmacokinetic properties, including high GI absorption, zero Lipinski violations, and a bioavailability score of 0.55.
Therefore, Quercetin was selected as the most promising lead compound for further visualization and analysis

## Visualization
Docked Complex Visualization
PyMOL visualization confirmed that Quercetin occupies the active-site binding pocket of Acetylcholinesterase (PDB ID: 4EY7). The ligand was observed within the binding cavity and surrounded by active-site residues, supporting the docking results obtained from AutoDock Vina.

## Key Findings

* EGCG showed the strongest binding affinity toward AChE.
* Quercetin demonstrated an excellent balance between docking performance and pharmacokinetic properties.
* Curcumin also showed strong binding affinity and favorable drug-likeness.
* Quercetin emerged as the most promising lead compound due to its high GI absorption, zero Lipinski violations, and good bioavailability.

--

## Visualization

Docking poses were visualized using PyMOL.

Visualization included:

* Protein cartoon representation
* Ligand stick representation
* Binding pocket inspection
* Active site interaction analysis


## Conclusion

The computational study identified Quercetin, Curcumin, and EGCG as promising nutraceutical inhibitors of Acetylcholinesterase. Among these, Quercetin demonstrated the most balanced profile by combining strong binding affinity with favorable pharmacokinetic characteristics. These findings suggest that Quercetin may serve as a potential lead molecule for future experimental validation and drug development studies.


## Software Used

* AutoDock Tools
* AutoDock Vina 1.2.4
* PyMOL
* SwissADME
* PubChem
* Protein Data Bank (PDB)
* Open Babel

## Future Work

* Protein-ligand interaction analysis
* Molecular dynamics simulations
* MM-PBSA/MM-GBSA binding energy calculations
* In vitro validation studies
 ## References
* Trott O, Olson AJ. AutoDock Vina: Improving the speed and accuracy of docking. Journal of Computational Chemistry, 2010.
* Daina A, Michielin O, Zoete V. SwissADME: A free web tool to evaluate pharmacokinetics and drug-likeness of small molecules. Scientific Reports, 2017.
* The PyMOL Molecular Graphics System.
* Protein Data Bank (PDB). https://www.rcsb.org
* PubChem Database. https://pubchem.ncbi.nlm.nih.gov


