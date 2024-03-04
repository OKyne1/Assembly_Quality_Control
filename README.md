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
2. [QUAST](https://github.com/ablab/quast) Nx/NGx

### 3. Completeness
1. [BUSCO](https://busco.ezlab.org/)
2. [CheckM](https://ecogenomics.github.io/CheckM/) (also detects contamination)

## Comparison to reference
In most cases of *de novo* genome assembly there is no reference availible for comparison. However, occasionally when developing new sequencing methods *de novo* assemblies can be compared to a reference genome. This makes quality assessments much simpler.

### Alignment and Visualisation
Alignment of the contigs/genome assembly to the reference is the simplest and best way to assess the success. For bacterial genomes, it is important to have genomes/contigs correctly rotated for alignment (e.g. using [circlator](https://sanger-pathogens.github.io/circlator/). Alignment can then be performed by tools like [minimap2](https://github.com/lh3/minimap2) to output a sorted indexed bam file. 

Visualisation of these bam files can be done using tools like [mauve](https://darlinglab.org/mauve/mauve.html) or [IGV](https://igv.org/).

### Dotplots
A fast but lower resolution method to compare these assemblies is using dotplots, performed in tools like [gepard](https://github.com/univieCUBE/gepard).

### Compare Assemblies
Ryan Wick developed a script, [compare_assemblies.py](https://github.com/rrwick/Perfect-bacterial-genome-tutorial/wiki/Comparing-assemblies), for comparing different assemblies (initially intended for assemblies pre-polishing and post-polishing). However, when assemblies are structurally very similar to the reference, it is possible to use this script to identify SNPs and INDELs found in the new assembly.

However, one challenge can be identifying which of these errors are true positives and which are false positives (i.e. wrong in the reference). One way to deal with this is to examine the evidence for these at a read level.


