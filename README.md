# Assembly Quality Control
This is a repository describing quality control methods and tools to assess genome assemblies.

## The 3 C's of Genome Assemblies
### 1. Correctness
Correctness is the base level accuracy of the assembly. The more correct the assembly, the fewer single nucleotide polymorphisms (SNPs) or insertions/deletions (INDELs) it will have.

Approaches to test correctness:
1. K-mer fequency based approaches (e.g. [yak](https://github.com/lh3/yak) and [merqury](https://github.com/marbl/merqury)) (this may need short reads - determine)
2. Frameshift detection using transcript data

### 2. Contiguity
1. N50/NG50
2. QUAST Nx/NGx

### 3. Completeness
1. [BUSCO](https://busco.ezlab.org/)
2. [CheckM](https://ecogenomics.github.io/CheckM/) (also detects contamination)


## Tools
### BUSCO
### Quast
### Alignment (to reference if availible)
### Contamination?
#### Checking reads (kraken and pavian)
#### Checking assemblies (?)
