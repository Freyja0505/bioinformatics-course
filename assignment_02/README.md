# Assignment 02 – Unix Command Line & GFF3 Analysis

## Course
FastTrack Bioinformatics 2025

## Objective
The goal of this assignment is to practice using Unix command line tools to explore and analyze genomic annotation data in GFF3 format.  
All analyses are performed in a reproducible manner using text-based Unix commands.

---

## Organism
**Drosophila melanogaster (fruit fly)**

Drosophila melanogaster is a well-established eukaryotic model organism commonly known as the fruit fly.  
It has been extensively used in genetics, developmental biology, and functional genomics.  
Its genome is relatively compact and well-annotated, making it suitable for practicing genomic annotation analysis using Unix-based workflows.

---

## Data Source
The GFF3 file used for this analysis was:
Drosophila_melanogaster.BDGP6.54.115.gff3.gz

obtained from the Ensembl public FTP site:

https://ftp.ensembl.org/pub/current_gff3/drosophila_melanogaster/

The data file itself is not included in this repository.  
Only the commands used to download and analyze the data are documented to ensure reproducibility.

---

## Methods
All analyses were conducted using standard Unix command-line tools including `curl`, `zcat`, `grep`, `awk`, `sort`, `uniq`, and `wc`.  
Pipelines were constructed using Unix pipes to allow streaming analysis without modifying the original data files.  
This approach ensures transparency, reproducibility, and minimal data handling overhead.

---

## Sequence regions
The GFF3 file contains a total of **1,870 sequence regions**, as defined by the `##sequence-region` entries.

Only a small subset of these correspond to the major chromosomes of *Drosophila melanogaster* (2L, 2R, 3L, 3R, X, Y, and chromosome 4).  
The remaining sequence regions represent unmapped scaffolds, minor contigs, mitochondrial genome, rDNA, and other assembled sequences.

This is consistent with expectations for a complex eukaryotic genome assembly, where many additional scaffolds are present beyond the primary chromosomes.

---

## Genes
Genes were identified as features with type `gene` in the third column of the GFF3 file.

A total of **13,986 genes** are annotated in the *Drosophila melanogaster* genome.

This gene count is consistent with expectations for a well-annotated model organism.  
It is important to note that the number of genes is smaller than the number of transcripts and exons, as individual genes can produce multiple transcripts through alternative splicing.

---

## Feature types
Feature types were identified from the third column of the GFF3 file and counted across the entire dataset.

The ten most abundant feature types include:

- exon (196,664 entries)
- CDS (163,288 entries)
- five_prime_UTR (46,792 entries)
- three_prime_UTR (33,741 entries)
- mRNA (30,802 entries)
- gene (13,986 entries)
- transposable_element_gene (5,896 entries)
- transposable_element (5,896 entries)
- ncRNA_gene (4,032 entries)
- ncRNA (3,060 entries)

Exon and CDS features are the most frequent, reflecting the multi-exon structure of eukaryotic genes.  
The presence of a large number of UTR annotations indicates a well-curated genome with detailed transcriptional regulation.

---

## Unfamiliar feature type
One feature type that may be less familiar is **transposable_element**, which represents mobile genetic elements capable of moving within the genome.

The relatively high number of transposable element annotations highlights the significant contribution of mobile elements to the *Drosophila* genome and its evolutionary dynamics.

---

## Overall assessment
Based on this analysis, the *Drosophila melanogaster* GFF3 annotation appears comprehensive and well-curated.  
The detailed representation of genes, transcripts, regulatory regions, and transposable elements reflects its status as a deeply studied and high-quality model organism genome.

