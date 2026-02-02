# Assignment 02 – Unix Command Line & GFF3 Analysis

## Course
FastTrack Bioinformatics 2025

## Objective
The goal of this assignment is to practice using Unix command line tools to explore and analyze genomic annotation data in GFF3 format.  
All analyses are performed in a reproducible manner using text-based Unix commands.

---

## Organism name: Drosophila melanogaster (fruit fly)

Drosophila melanogaster is a well-established eukaryotic model organism commonly known as the fruit fly.
It has been extensively used in genetics, developmental biology, and functional genomics.
Its genome is relatively compact and well-annotated, making it suitable for practicing genomic annotation analysis using Unix-based workflows.

---

## Data Source

The GFF3 file used for this analysis was:
Drosophila_melanogaster.BDGP6.54.115.gff3.gz
obtained from the Ensembl public FTP site under:
https://ftp.ensembl.org/pub/current_gff3/drosophila_melanogaster/

---

## Methods
All analyses were conducted using Unix com

---

## Sequence regions

The GFF3 file contains a total of 1870 sequence regions as defined by the `##sequence-region` entries.

Only a small subset of these correspond to the major chromosomes of Drosophila melanogaster (2L, 2R, 3L, 3R, X, Y, and chromosome 4).
The remaining sequence regions represent unmapped scaffolds, minor contigs, mitochondrial genome, and other assembled sequences.

This is consistent with expectations for a complex eukaryotic genome assembly, where many additional scaffolds are present beyond the primary chromosomes.
