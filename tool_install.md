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

3.gappa
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

# Orthofinder
https://orthofinder.github.io/OrthoFinder/

Orthofinder was installed through a conda environment

```bash
conda create -n of3_env python=3.12
conda activate of3_env
conda install -c conda-forge -c bioconda orthofinder
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




