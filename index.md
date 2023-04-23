# Trevor Harrington's Github Homepage
Undergraduate repository containing  RStudio workbooks created in Bioinformatics BIO-4ST1-14708

This page will contain three Rstudio projects in order of my progress using coding tools. Palmer_penguine dataset was used to initially understand how to utilize RStudio for data cleaning and analysis. Invertebrates was an attempt to first explore a unknown dataset that was less-then-friendly for a new coder to manipulate and interpret. 
The most significant piece of work contained in this page is the analysis of indoor pollution representing a percentage of deaths in countries across the globe.


---
## Statistical Analysis: Basic Functions

### Introduction
  This journal contains some useful examples of how to run basic statistics functions using the base RStudio software. These workbook have been developed over the first half of ENV 220 Field Methods and Technologies. The methods of statistical analysis that are described in this section include functions for linear regression, t-testing and ANOVA testing. These resources are valuable for understanding the coding and statistical formulas that can be used in RStudio to make inferential statements from a dataset.
  
  ### [linear Regression](https://tmharrington.github.io/FieldMethodsandTechnologies/Lin_Regression_in_RStudio.html)
  ### [T-testing](https://tmharrington.github.io/FieldMethodsandTechnologies/T_Test_in_RStudio.html)
  ### [ANOVA](https://tmharrington.github.io/FieldMethodsandTechnologies/ANOVA_in_RStudio.html)
  
  
---
## Palmer Penguines analysis

### Abstract
  This Workbook contains an analysis of Palmer Penguins to determine correlations present in the dataset containing 8 variables including year, region, gender, and physical characteristics like bill length and height, body mass, and flipper length. A exploratory dataset was generated using a random set of half the total variables to find any potential correlations that can be inferred with the full dataset. Statistical analysis was performed in tables and graphs, and found several interesting correlations, including that between species and island, species and bill length, and between flipper size and bill length for gentoo penguins.   

### [Analysis](https://tmharrington.github.io/BioStatisticalAnalysis/PalmerPenguins_Initial.html)


---
## Invertebrate analysis

  This notebook is used to investigate the practice of data cleaning and organizing. The dataset was gathered by Dr. Duryea at Lamoille Creek in Lamoille, NV. 

### Abstract

### [Analysis](https://tmharrington.github.io/BioStatisticalAnalysis/InvertAnalysis.html)


---
## Indoor Air Pollution analysis

### Abstract
This research paper investigates the impact of indoor air pollution on premature deaths and its correlation with factors such as GDP, population size, and region. The paper highlights indoor air pollution’s significant risk to public health, particularly in low-income countries, and the need for targeted interventions to address the issue. The analysis finds that regional factors are crucial in determining indoor air pollution prevalence and associated health risks. While economic development can help reduce indoor air pollution, it can also create new sources of pollution. The analysis emphasizes the need for a nuanced understanding of the issue and further research to develop effective policies and interventions.

### [Analysis](https://tmharrington.github.io/BioStatisticalAnalysis/IndoorPollution.html)


---
## SNHU Arboretum Stream Pollution Analysis

### Abstract
This study aimed to evaluate the impact of water source proximity on tree size and estimate carbon sequestration in the SNHU Arboretum. Two 5x5 meter plots were selected, one near a seasonal second-order stream and the other distant from it. Diameter at breast height (DBH) was measured for five trees in each plot, and biomass was estimated using the allometric scaling equation. Tree density was calculated to estimate the amount of CO2 sequestered by the arboretum. The t-test revealed no significant difference between the mean DBH of trees near water (mean = 37.36 cm) and those distant from water (mean = 45.32 cm) at the 95% confidence level. The small sample size may have affected the results, suggesting that a larger sample size and tree height measurements could improve accuracy. This study serves as a low-confidence example of CO2 calculation but accurately illustrates the process.

### [Part 1: DBH Comparison](https://tmharrington.github.io/FieldMethodsandTechnologies/Pollution_Project_Part_1.html)
### [Part 2: Soil Sample Analysis](https://tmharrington.github.io/FieldMethodsandTechnologies/Arboretum_Project_2.html)

---
## Bioinformatics: Replication Origin Analysis

As a student delving into the fascinating world of genomics, this RMarkdown showcases the code built over the semester that explores various functions and techniques for analyzing genomic patterns. This document aims to provide a comprehensive guide for understanding and identifying the replication origin of bacterial genomes using RStudio.

The RMarkdown document covers a range of essential topics and functions over six chapters, which build the knowledge and tools needed to utilize RStudio in the pursuit of uncovering patterns in a bacterial genome. Bacterial genomes range in length, but can easily exceed lengths that these methods can quickly process; for this reason, randomized genomes and Rosalalind Challenges will be used to identify that code works successfully. The goal of this  

- **Chapter One**  Opens with demonstrating how to generate a randomized sequence of nucleotides in a vector array, followed by an introduction to loops. The `randomized genome` will be utilized throughout this notebook for testing the functions created before applying them to an entire genome. 
  This chapter closes with an introduction to **Rosalind Challenges** which will help identify that the functions generated will work successfully if applied to a longer genome. After identifying functionality of the `Sum Nucleotides` code that calculates how many of each nucleotide is present, the code is used to calculates the sums for a **Vibrio Cholera genome**.

- **Chapter Two** Begins with learning how to use functions in R to save the codes developed for future use, begining with `rnd_genome` that outputs the same randomized genome as developed in chapter 1. The chapter begins applying the genome for segmenting the data by different lengths, ending in a `generate_k_mers" and `nt_pattern`, which finds k-mers that match an user-input string. This code was successfull when testing with the **Rosalind Challenge**, but never tested on a genome. 

- **Chapter Three** Introduces **Complementary Strands** and how to generate them for a randomized genome. Complementary strands are antiparrelel, meaning the string must be both flipped in direction (5' -> 3') as well as replaced with the complementary nucleotide. 

- **Chapter Four** Introduces `Clump Finding` function, which is designed to look for repeating sequences of nucleotides inside a window of a user-defined length within a genome. This function is necessary to locate the *Origin of Replication* (OriC) identified with the **dnaA box**. DnaA boxes are specific DNA sequences that are recognized by the DnaA protein, which plays a crucial role in initiating DNA replication in bacteria. The binding of DnaA to these boxes helps to unwind and separate the DNA strands, allowing for the replication machinery to begin copying the DNA. The number and location of DnaA boxes can vary among bacterial species, but they are generally located near the origin of replication.

  - While this code did successfully complete the Rosalind string, the attempt to run it on a **E Coli genome** proved unsuccessfull do to the length of time required work through the genome without improving computational efficiency. A number of methods could be used to improve the run-time of this code, namely changing the character string into a numerical vector, or introducting a R package like `Stringr` or `Stringi`. 

- **Chapter Five** Provides a introduction to `skew`, and contains the only visualizion used to demonstrate the biology of these concepts. In DNA sequencing, **skew** refers to the difference in frequency between two nucleotides (typically Guanine and Cytosine) along a DNA sequence. By calculating the "GC skew" (i.e., the difference between the frequency of G and C nucleotides), it is possible to identify a region of the genome where the skew changes from positive to negative, which often indicates the location of the origin of replication. the graph shows the skew for the **E Coli genome** which provides a very clear visual example of how this method can be utilized to identify a specific region of the genome where the Origin of Replication is most likely to be found.

- **Chapter Six** Is the final chapter of this notebook, and introduces a `Hamming Distance` function that can identify the difference between two strings being compared. This code can account for mutations in a bacterial genome, and provide a user defined tolerance for how many mutations are permitted. Hamming distance is then used to improve the functionality of `Nucleotide Pattern` function to search through a genome with a tollerance for mutations. This step, combined with skew, will be critical for improving the functionality of the `clump finding` function by both improving the recognition (`hamming distances`) and narrowing the search field (`skew`).

### [Workbook](https://agmath.github.io/BIO4ST1_Group1/Replication_Trevor_Harrington.html)


