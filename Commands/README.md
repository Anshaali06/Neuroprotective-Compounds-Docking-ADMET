# Commands Used

## 1. Protein Preparation (PyMOL)

```pymol
remove solvent
remove resn E20
save 4EY7_clean.pdb
```

Output:

```text
Remove: eliminated 552 atoms in model "4EY7"
Remove: eliminated 56 atoms in model "4EY7"
```

## 2. Receptor Preparation (AutoDock Tools)

- Load 4EY7_clean.pdb
- Edit → Hydrogens → Add → Polar Only
- Edit → Charges → Compute Gasteiger
- Grid → Macromolecule → Choose Molecule
- Save as:

```text
4EY7_clean1.pdbqt
```

## 3. Ligand Preparation

### Open Babel

```powershell
obabel ligand.sdf -O ligand.pdb
```

### AutoDock Tools

- Load ligand.pdb
- Add Hydrogens
- Compute Gasteiger Charges
- Detect Root and Rotatable Bonds
- Save as ligand.pdbqt

- ## 4. Grid Center Calculation (PyMOL)

```pymol
select ligand, resn E20
print(cmd.centerofmass("ligand"))
```

Output:

```text
[-1.6241149361476006, -50.09128532940734, 2.0558886275481623]
```

## 5. Molecular Docking

### Batch Docking Script

```powershell
$ligands = @(
"Curcumin",
"DHA",
"EPA",
"Resveratrol",
"Quercetin",
"EGCG"
)

foreach ($l in $ligands) {
    .\vina_1.2.4_win.exe --config config.txt --ligand "$l.pdbqt" --out "${l}_out.pdbqt"
}
```

## 6. Visualization (PyMOL)

```pymol
hide everything

show cartoon, 4EY7_clean1
color cyan, 4EY7_clean1

show sticks, Quercetin_out
color yellow, Quercetin_out

zoom Quercetin_out, 8

select pocket, byres (4EY7_clean1 within 4 of Quercetin_out)
show sticks, pocket
color green, pocket

set cartoon_transparency, 0.2

bg_color white

ray

png Quercetin_Docking_Final.png, dpi=300
```
