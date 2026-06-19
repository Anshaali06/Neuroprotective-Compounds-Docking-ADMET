# Neuroprotective-Compounds-Docking-ADMET
An in-silico molecular docking and ADMET analysis study evaluating the binding affinity of six neuroprotective compounds against a pesticide-induced neurotoxicity target protein (PDB ID: 4EY7).
## Project Overview
This project focuses on the computational screening of six neuroprotective compounds (DHA, EPA, Curcumin, Resveratrol, Quercetin, and EGCG) against a pesticide-induced neurotoxicity target protein (PDB ID: 4EY7). Molecular docking was performed using AutoDock Vina to evaluate the binding affinity of the selected compounds toward the target protein. The docking results were further supported by ADMET analysis to assess the drug-likeness and pharmacokinetic properties of the compounds. Protein–ligand interactions of the top-performing candidate were visualized using PyMOL. Comparative analysis identified EGCG as the strongest binder, followed by Quercetin and Curcumin, highlighting their potential as neuroprotective candidates for further investigation.

 ## Methodology
1. Retrieved six neuroprotective compounds (DHA, EPA, Curcumin, Resveratrol, Quercetin, and EGCG) from PubChem.
2. Retrieved the target protein structure (PDB ID: 4EY7) from the Protein Data Bank.
3. Cleaned and prepared the protein structure using PyMOL.
4. Converted ligand structures from SDF to PDB format using Open Babel.
5. Performed molecular docking using AutoDock Vina.
6. Evaluated ADMET properties using SwissADME.
7. Visualized protein–ligand interactions of the top-performing compound using PyMOL.

## Tools Used
- PubChem 
- Protein Data Bank (PDB) 
- Open Babel 
- PyMOL 
- AutoDock Vina 
- SwissADME 
