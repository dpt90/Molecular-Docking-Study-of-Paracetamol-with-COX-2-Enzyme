[Binding_Site_Residues.txt](https://github.com/user-attachments/files/24106798/Binding_Site_Residues.txt)[PyRx_docking _file.csv](https://github.com/user-attachments/files/24106745/PyRx_docking._file.csv)# Molecular-Docking-Study-of-Paracetamol-with-COX-2-Enzyme


## **1. Introduction**

This project presents a complete computational docking workflow to analyze the interaction between **Paracetamol (Acetaminophen)** and the **Cyclooxygenase‑2 (COX‑2) enzyme**. Molecular docking is a key method in computational chemistry used to predict how a small molecule (ligand) binds to a macromolecular target (protein). The primary objective is to estimate binding affinity, identify interacting residues, and visualize the binding mode.

This study uses freely available tools, making it fully reproducible.

---

## **2. Objective**

To determine the binding affinity and molecular interaction pattern of **Paracetamol** when docked inside the **COX‑2 enzyme active site (PDB ID: 5IKR)** using computational docking techniques.

---

## **3. Software Used**

The following open‑source tools were used:

### **Ligand Preparation**

* **Avogadro** – drawing and optimizing ligand geometry
* **MMFF94 force field** for energy minimization

  

### **Docking Simulation**

* **PyRx (AutoDock Vina backend)** – docking engine and scoring

### **Visualization & Analysis**

* **UCSF Chimera** – protein–ligand interaction visualization
* (Optional) **Discovery Studio Visualizer** 

All software is freely available for academic use.

---

## **4. Methodology**

### **4.1 Ligand Preparation**

1. Paracetamol structure was created in **Avogadro**.
2. Geometry optimization was performed using **MMFF94**.
3. The ligand was exported as **.mol2** file.

### **4.2 Protein Preparation (COX‑2: PDB 5IKR)**

1. Protein downloaded from **RCSB Protein Data Bank**.
2. Loaded in **Chimera** for cleaning:

   * Removed: water molecules, ions, unwanted ligand fragments.
   * Added hydrogens.
3. Saved as **clean_protein.pdb**.

### **4.3 Docking Using PyRx (AutoDock Vina)**

1. Imported ligand (.mol2) and protein (.pdb) into PyRx.
2. Converted both to **.pdbqt** format.
3. Defined docking search space around the COX‑2 active site.
4. Ran AutoDock Vina simulation.
5. Obtained ranked poses and binding energies.
6. Exported lowest‑energy pose as **best_pose.pdb**.

<img width="1130" height="421" alt="snapshot1" src="https://github.com/user-attachments/assets/338fc9fd-5f8c-424e-862f-fe1d59067d8e" />


### **4.4 Visualization & Interaction Analysis (Chimera)**

1. Opened **protein** and **docked ligand** together.
2. Displayed:

   * Protein as ribbon
   * Ligand as stick model
3. Identified H‑bonds using *FindHBond* tool.
4. Identified binding pocket residues using *Zone Selection*.
5. Saved:

   * Complex visualization image
<img width="1920" height="950" alt="iDocking_Complex" src="https://github.com/user-attachments/assets/d17de57b-697d-411b-bde0-f22631eecf1a" />



   * Hydrogen bond map ( green colour bond )
<img width="1920" height="950" alt="Hydrogen_Bond_Interactions" src="https://github.com/user-attachments/assets/9c98b28a-b8ca-412b-822e-858678688dc7" />



   * Interaction residue list
     [U#0 GLY 225.A O
#0 GLY 227.A C
#0 GLY 227.A CA
#0 GLY 227.A HA2
#0 GLY 227.A HA3
#0 VAL 228.A C
#0 VAL 228.A CA
#0 VAL 228.A CB
#0 VAL 228.A CG2
#0 VAL 228.A H
#0 VAL 228.A HA
#0 VAL 228.A HB
#0 VAL 228.A HG23
#0 VAL 228.A N
#0 VAL 228.A O
#0 GLN 374.A C
#0 GLN 374.A CA
#0 GLN 374.A CB
#0 GLN 374.A HA
#0 GLN 374.A HB2
#0 GLN 374.A HB3
#0 ASN 375.A C
#0 ASN 375.A CA
#0 ASN 375.A CB
#0 ASN 375.A H
#0 ASN 375.A HB2
#0 ASN 375.A HB3
#0 ASN 375.A N
#0 ASN 375.A O
#0 GLY 533.A O
#0 GLY 536.A C
#0 GLY 536.A O
#0 ASN 537.A CA
#0 ASN 537.A CB
#0 ASN 537.A CG
#0 ASN 537.A HA
#0 ASN 537.A HB2
#0 ASN 537.A HD21
#0 ASN 537.A HD22
#0 ASN 537.A N
#0 ASN 537.A ND2
#0 HOH 756.A O
#0 HOH 777.A O
#0 HOH 797.A O
#0 HOH 816.A O
#0 HOH 845.A O
#0 HOH 901.A O
#0 HOH 920.A O
#0 HOH 938.A O
#0 HOH 949.A O
#0 HOH 958.A O
#0 TRP 139.B CH2
#0 TRP 139.B HH2
#0 TRP 139.B HZ2
#0 PHE 142.B CE1
#0 PHE 142.B CE2
#0 PHE 142.B CZ
#0 PHE 142.B HE1
#0 PHE 142.B HE2
#0 PHE 142.B HZ
#0 HOH 798.B O
#0 HOH 844.B O
#0 HOH 893.B O
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het C
#1 LIG 1.het H
#1 LIG 1.het H
#1 LIG 1.het N
#1 LIG 1.het O
#1 LIG 1.het O
ploading Binding_Site_Residues.txt…]()

   * Final complex PDB file

---

## **5. Results**

### **5.1 Docking Score**

The lowest binding energy obtained from **AutoDock Vina** represents the most stable protein–ligand complex.



[UploadiLigand,Binding Affinity,rmsd/ub, rmsd/lb
my_COX2_clean_paracetamol,-5.9,0.0,0.0
my_COX2_clean_paracetamol,-5.9,14.568,10.911
my_COX2_clean_paracetamol,-5.8,3.787,2.761
my_COX2_clean_paracetamol,-5.7,11.954,10.907
my_COX2_clean_paracetamol,-5.4,11.189,9.544
my_COX2_clean_paracetamol,-5.4,5.353,3.935
my_COX2_clean_paracetamol,-5.4,5.565,2.549
my_COX2_clean_paracetamol,-5.3,9.805,6.798
my_COX2_clean_paracetamol,-5.3,12.141,10.14
ng PyRx_docking _file.csv…]()



### **5.2 Protein–Ligand Interaction Analysis**

Key interactions identified:

* Hydrogen bonds between paracetamol and active‑site residues
* Hydrophobic contacts stabilizing the ligand
* Aromatic (pi–pi) interactions (if observed)

### **5.3 Binding Pocket Residues**

Residues within 4 Å of the ligand (examples; replace with your output):

* ARG120
* TYR355
* VAL349
* ALA527

### **5.4 Visualization Outputs**

Included outputs:

* Docked complex (protein + ligand) image
* Hydrogen bond interaction map
* Final combined PDB file
* 2D interaction diagram (if generated)

---

## **6. Discussion**

The docking score and interaction profile indicate that Paracetamol binds favorably to the COX‑2 active site. Hydrogen bonding plays a major role in stabilizing the complex, along with hydrophobic pocket interactions. These results align with the known biological function of Paracetamol as a COX inhibitor.

The study demonstrates the capability of computational docking tools to predict molecular interactions and guide drug‑target understanding.

---

## **7. Conclusion**

This project successfully performed a complete molecular docking workflow to evaluate Paracetamol's interaction with COX‑2. The computed binding affinity and visual interaction analysis support the molecule's inhibitory behavior. The approach is reproducible and can be extended to other ligands or protein targets.

---

## **8. How to Reproduce This Study**

Clone this repository and follow the workflow:

```bash
git clone <your-repo-url>
cd docking-paracetamol-cox2
```

Ensure the following files are included:

* `paracetamol.mol2`
* `cleaned_5ikr.pdb`
* `best_pose.pdb`
* `protein_ligand_complex.pdb`
* `results/` (images, interaction maps, CSV docking output)

---

## **9. References**

* Trott O., Olson A. J. *AutoDock Vina: improving the speed and accuracy of docking.* J Comput Chem.
* UCSF Chimera documentation
* Avogadro molecular editor
* RCSB Protein Data Bank

---

### **Author**

*Your Name Here*

If you want, I can also generate:

* A short abstract
* A GitHub repository folder structure
* Image captions and figure numbering
* A PDF‑formatted report

Just let me know what you want to add.
