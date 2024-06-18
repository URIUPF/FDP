Final Degree Project: Metagenomics Analysis
Overview
Welcome to the repository for my final degree project in metagenomics. This project aims to analyze microbial communities using various bioinformatics tools and pipelines. Here you will find scripts and workflows used in the analysis, organized by different aspects of the project.

Study Description
In this study, building on the samples collected in the previous study, the genomic data underwent analysis employing various tools within the metaWRAP pipeline.

Title: Unravelling the Nasal Microbiome of Piglets Through Whole Genome Metagenomics Sequencing

Experimental Groups
Table 1 represents the groups used in the study:

Sow Treatment	Piglet Treatment	Group
Treated Sow (TS)	Non-treated piglet (NTP)	TS-NTP
Inoculated piglet (IP)	TS-IP
Non-treated Sow (NTS)	Inoculated piglet (IP)	NTS-IP
Treated piglet (TP)	NTS-TP
Non-treated piglet (NTP)	NTS-NTP*
*Control group.

Analysis Workflow
Quality Control and Processing
Quality control and preprocessing were conducted on the raw sequence reads to ensure the integrity and accuracy of the data. Trim-Galore (integrating Cutadapt and FastQC) was employed to trim and preprocess the sequences, removing low-quality bases and adapter sequences. Additionally, bmtagger alongside the Sus scrofa reference genome v11.1 was used to systematically eliminate any reads corresponding to the host genome. Quality reports were generated for each sequenced sample.

Read Assembly
The assembly of high-quality, preprocessed reads was executed utilizing MetaSPAdes. The resultant contigs encapsulate the genetic material retrieved from our metagenomic samples and are integral for further exploration.

Taxonomic Profiling and Diversity Analysis
Taxonomic profiling of the metagenome-assembled contigs was performed using Kraken 2. Krona was used to visualize and generate plots of all the taxa found in the metagenomic samples. Alpha and beta diversity analyses were performed to assess differences between groups after weaning (D21) and the final extraction day (D49). The Kruskal-Wallis test was used to evaluate the impact of distinct treatments on alpha diversity indices across piglet groups. PERMANOVA was employed to examine dissimilarity in microbial communities between samples.

Metagenomic Fragment Binning and Quantification
Binning is the process of grouping together fragments of sequenced DNA believed to originate from the same genome, thus reconstructing the genomes of individual microbial species from metagenomic data. In this study, the assembly was binned with metaBAT2. The quality of the resulting metagenome-assembled genomes (MAGs) was evaluated using CheckM. Abundance quantification of the MAGs was performed using Salmon to determine the distribution and relative abundance of the reconstructed genomes.

Classification and Annotation of MAGs for Protein Prediction
Functional annotation of genomes and proteins was conducted using PROKKA to explore potential roles and metabolic capabilities within the bacterial community. Subsequently, SignalP was employed to predict secreted proteins.

Data Processing and R Analysis
Subsequent analyses of the outputs, data preparation, table creation, and plotting were conducted using RStudio. The following packages were utilized: vegan, ggplot2, dplyr, tidyr, and stringr.

Folders and Contents
KRAKEN
Description: Scripts and outputs related to Kraken taxonomic classification.
Last Update: 16 minutes ago
Key Files:
Run_Kraken.slm: Script to run Kraken for taxonomic classification.
MetaWRAP
Description: Scripts and outputs related to MetaWRAP pipeline for metagenomic assembly and binning.
Last Update: 18 minutes ago
Key Files:
DRAFT_ALL_full_pipeline.slm: Script for the MetaWRAP pipeline.
PROKKA
Description: Scripts and outputs related to Prokka for bacterial genome annotation.
Last Update: 9 minutes ago
Key Files:
Run_Prokka_Colonizers.slm: Script to run Prokka for annotation of bacterial genomes.
RSTUDIO
Description: Contains files related to RStudio for statistical analysis and visualization.
Last Update: just now
Key Files:
(Specify key files if known)
SignalP
Description: Scripts related to protein prediction using SignalP.
Last Update: (Specify)
