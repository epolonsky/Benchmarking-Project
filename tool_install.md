# SHOOT
https://github.com/davidemms/SHOOT

The following dependencies were installed for this tool:

1. DIAMOND
```bash
conda install -c conda-forge -c bioconda diamond
````

2. MAFFT
```bash
conda install -c bioconda mafft
```

3. gappa
```bash
conda install -c bioconda gappa
```

4. epa-ng
```bash
conda install -c bioconda epa-ng
```

The following python dependencies were installed for this tool:
* ete3
* scikit-learn
* biopython
* pytest
* six

clone the SHOOT github repo

```
git clone https://github.com/davidemms/SHOOT
```

run using the same test data as for orthofinder

```bash
conda activate of3_env
orthofinder -f orthofinder_test_data/ -M msa -o shoot_test_data
PYTHONPATH="$PWD/SHOOT" python SHOOT/shoot/create_shoot_db.py shoot_test_data/Results_Sep21 full
PYTHONPATH="$PWD/SHOOT" python SHOOT/shoot/bifurcating_trees.py shoot_test_data/Results_Sep21
ln -s profile_sequences.all.fa.db.dmnd shoot_test_data/Results_Sep21/diamond_profile_sequences.fa.db.dmnd
PYTHONPATH="$PWD/SHOOT:$PWD/SHOOT/shoot" python -m shoot orthofinder_test_data/Mycoplasma_agalactiae.faa shoot_test_data/Results_Sep21/
```

# Orthofinder
https://orthofinder.github.io/OrthoFinder/

Orthofinder was installed through a conda environment

```bash
conda create -n of3_env python=3.12
conda activate of3_env
conda install -c conda-forge -c bioconda orthofinder
conda install numpy=1.26.4
```

run test data

```bash
conda activate of3_env
orthofinder -f orthofinder_test_data/
```

# OrthoLoger
https://orthologer.ezlab.org/

https://bioconda.github.io/recipes/orthologer/README.html

This is not currently working - will try to install through docker maybe
```bash
conda install -c conda-forge -c bioconda orthologer
```

# proteinortho

```bash
conda create -n proteinortho_env -c conda-forge -c bioconda python=3.7 proteinortho
```

run test data

```bash
conda activate proteinortho_env
perl proteinortho6.pl -project= proteinortho_test_data/ proteinortho_test_data/C.faa proteinortho_test_data/E.faa proteinortho_test_data/L.faa proteinortho_test_data/M.faa
```




