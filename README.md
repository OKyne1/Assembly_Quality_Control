# Assembly Quality Control
This is a repository describing quality control methods and tools to assess genome assemblies.

## The 3 C's of Genome Assemblies
### 1. Correctness
Correctness is the base level accuracy of the assembly. The more correct the assembly, the fewer single nucleotide polymorphisms (SNPs) or insertions/deletions (INDELs) it will have.

Approaches to test correctness:
1. K-mer fequency based approaches (e.g. [yak](https://github.com/lh3/yak) and [merqury](https://github.com/marbl/merqury))

### 2. Contiguity
### 3. Completeness

## Metrics
N50, NG50 etc

## Tools
### BUSCO
### Quast
### Alignment (to reference if availible)
### Contamination?
#### Checking reads (kraken and pavian)
#### Checking assemblies (?)
