# Semester Project

**Name**: Ruben Lerma-Reyes  
**Course**: Intro to Scientific Programing  
**Semester**: Spring 2019  
**Assignment**: Semester Project Proposal

## Designing a Script to Sort Lipidomics Data by Intensity and Between Samples   

Background & Rationale: GLABRA2 (Gl2) is a class IV Homeodomain (HD) Leucine Zipper (ZIP) transcription factor. These transcription factors are unique becase of the presence of a lipid/sterol binding Steroidagenic Acute Regulatory (StAR) Protein-related Lipid Transfer (START) domain that is found in tandem with a DNA-binding homeodomain [1]. The combination of these domains is only found in the plant kingdom and presents the possibility for transcriptional regulation that is influenced by lipid/sterol binding. The Schrick lab is interested in identifying the putative lipid binding partners for GL2. By using *in vitro* cell-free approach, a protein of interest can be isolated using affinity purification through application of a HALO tag attached to magnetic beads. Then this purified protein is incubated with a lipid extract prepared from *Arabidopsis thaliana* materials. Unbound lipids were washed away, meanwhile those that remained by virtue of their interaction with the protein were analyzed using LC/MS for identification. Five different samples were subjected to this experimental design. The samples include a negative control containing just the HALO vector alone (negative control), GL2, GL2 with the START domain deleted, an unrelated lipid binding protein ROSY1, and the lipid extract without protein presence. The spectral data obtained has already been processed, where each peak that was present represents a possible lipid of interest and was assigned an intensity value. This is tabulated in an excel spreadsheet that contains the data for all five samples. By removing the hits (peaks) that arise in our controls and setting a threshold value for the fold difference in intensity, true candidate binding lipids for GL2 can isolated. For example, a lipid binding to the empty HALO tag and also GL2 is not a true candidate because it does not reflect GL2's affinity for said protein and is an artifact that must be removed from consideration. While lipids that bind to both GL2 and GL2 without START could be indicative of lipid binding unrelated but relevant at an alternate domain. It is important to note that the data for the *A. thaliana* extract has mostly known identities but that there was plenty of other hits arising from an unknown source and with no obvious identity. While still possibly useful information, it is necessary to separate out these data from more relevant peaks. 

Objective: To write a Python script that automates the comparison of data sets from different samples to determine binding partners of a purified protein of interest that is above a certain threshold. This python script should be flexible enough that it could be applied to future analyses of data obtained from similar experiments. While also being able to analyze both the "positive" and "negative" mode data that is obtained from the LC/MS instrument. Once replicates for this experiment is obtained, functions for calculating the mean, standard deviation, and statistical signifance of these peaks would also be included in the script. 

Outcomes: A sorted list of values in a .csv file that identifies candidate lipid binding ligands for our protein of interest. The data would be sorted based on intensity and the statistical likelihood. It would show which lipids overlap between sets and whether the intensity value is sufficiently high to be considered relevant. This script would lead to easy and automatic interpertation of LC/MS data. 

Sketch:
        
<img src="Semester-Project/semester project sketch.jpg" width="500"/>


References: 1. K. Schrick, D. Nguyen, W. M. Karlowki, K. FX. Mayer. (2004). START lipid/sterol-binding domains are amplified in plants and are predominantly associated with homeodomain transcription factors. Genome Biology **5(6): R41**
