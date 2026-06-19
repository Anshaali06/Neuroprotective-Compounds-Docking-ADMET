# Commands Used

## Batch Docking (PowerShell)

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
    Write-Host "Running $l ..."
    .\vina_1.2.4_win.exe --config config.txt --ligand "$l.pdbqt" --out "${l}_out.pdbqt"
}
```

## PyMOL Commands

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

hide labels

set cartoon_transparency, 0.2

bg_color white

ray

png Quercetin_Docking_Final.png, dpi=300
```

## Open Babel

```powershell
obabel ligand.sdf -O ligand.pdb
```
