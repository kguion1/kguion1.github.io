---
layout: page
title: "1.4 Introduction to -omics"
permalink: /Intro_Public_Data/
---

## What are the "-omics"?
"-omics" refers to data generated from different pools of biological molecules. For example, *genomics* refers to data arising from DNA, *transcriptomics* refers to RNA data, and *proteomics* refers to protein data. 
While there are many other -omics, these three will be focused on in this curriculum. You can notice that genomics, transcriptomics, proteomics follow the central dogma of biology. Depending on your biological background, you may be familiar with this concept. If you need a refresher, check out this [khan academy article](https://www.khanacademy.org/science/ap-biology/gene-expression-and-regulation/translation/a/intro-to-gene-expression-central-dogma).  

As the central dogma requires the flow from DNA to RNA to protein, you might assume that we should just study DNA and everything else will follow. However, research has shown that DNA, RNA, and protein data is not always as consistent as theory suggests. This may be due to a variety of factors that range from biological, or events that do occur in the cell, to experimental, or limitations of our data-measuring techniques. 
Because of this inconsistency across the central dogma, analyzing multiple types of data provides more information on the true biological state.

This curriculum teaches analysis of three individual -omics; however, it is our hope that understanding indivdiual analyses pushes you to consider a "multi-omic" approach. Starting with individual -omics allows you to understand the strengths, limitations, and challenges of each -omic so that you can more appropriately consider how to combine these different -omics.

## Levels of Data
Levels of data refers to the different data generated **within** a single -omic. There is not just one "genomic data file" or one "transcriptomic data file". Instead multiple *levels* of genomic data are generated and can be analyzed. The same could be said for transcriptomic and proteomic data types. While different scientists may have different definitions of "levels of data", it is an important concept to recognize. The following are general definitions of each level that will be used throughout his course. 

1. Raw data generated from experimental technique
2. Basic processing. May included quality control, low level interpretation, normalization, etc.
3. Further processing that provides biological meaning
4. Results of "downstream" analysis

**We will be using Level 3 data**. Analyzing Level 1 and Level 2 data is still an important field of research the focuses on providing high quality Level 3 data. This will not be covered in this curriculum.

Below are examples from the three omics we are discussing. 

#### Genomics
1. Sequencing of gene. This is a large file of A's, T's, C's, and G's. 
2. Quality assesed gene sequence. Sequencing techniques are not error free. In moving from level 1 to level 2, algorithms exist that attempt to decrease error of the gene sequence as much as possible. 
3. Mutation or copy number data. To move from level 2 to level 3, the genetic sequence is compared to a "reference genome" and mutations or copy number variants (multiple or deleted copies of genes) are identified. 
4. Analysis that relates data to biological conclusion. For example, men might have more mutations in one gene than females.

#### Transcriptomics
1. Sequencing of RNA transcript. This is a large file of A's, T's, C's, and G's. 
2. Sequence is mapped to a reference genome to result in the number of transcripts for each gene
