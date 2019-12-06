# Final_Project
The Final Project R Markdown file and the html output file is uploaded in the Milestones folder. The final project Rpubs file can be viewed here [Final Project](http://rpubs.com/psehgal0504/557086). 

## Description
Runx2 is a transcription factor that is overexpressed and promotes metastasis in breast cancer. In our pilot study we have shown that Runx2 undergoes post-translational modification. WT was found to promote TGF beta induced migration and invasion but this ability was lost in case of the modification deficient mutant generated in the lab. The data suggests that this post-translational mofification of Runx2 WT might promote metastasis. 

## Datasets
The ChIp-seq was done on 4 samples out of which 2 were inputs. I do not have repliactes for the samples. The data was generated for 2 MDA-MB-231 breast cancer lines expressing Runx2 WT and Runx2 mutant and their respective inputs for normalization. I am starting with peaks data generated by MACS2.

WT peak dataset

<img src="https://github.com/psehgal0504/Final_Project/blob/master/Images/WT_dataset.png" width="500">

Mutant peak dataset

<img src="https://github.com/psehgal0504/Final_Project/blob/master/Images/Mutant_dataset.png" width="500">

## Proposed Analysis
I want to look at binding pattern differences between the WT and mutant Runx2.
For this I have four questions that I want to answer:
1. What regulatory elements are bound by the WT and the mutant?
2. Runx2 WT and mutant binding to TSS regions?
3. How is the enrichment of the protein binding is affected across the chromosomes for WT and mutant?
4. Functional enrichment analysis for WT and mutant?

I will be using the ChIP-seq specific R Bioconductor packages to do my ChIP-seq analysis. 
```{r}
library(ChIPseeker)
library(ChIPpeakAnno)
library(TxDb.Hsapiens.UCSC.hg38.knownGene)
library(clusterProfiler)
library(ReactomePA)
library(org.Hs.eg.db)
library(GenomicFeatures)
library(GenomicRanges)
library(ggplot2)
```

## Proposed Timeline & Major milestones (or segments).
Milestone 1 (11/14/2019): Get familiar with using the ChIPseeker package by working with a known data set. Try to get the result for the first two problems.
Milestone 2 (11/21/2019): Continue with understanding the package and answer the last two questions.
Milestone 3 (11/27/2019): Optimizing the results and overcome any road blocks hit. Submit a rough draft for QA. 
Milestone 4 (12/06/2019): Address the QA problems and make the final draft. Submit the final project.

## User Interface
Some of the expected results should look like this.

<img src="https://github.com/psehgal0504/Final_Project/blob/master/Images/Annotate_peaks.jpg" width="500">

<img src="https://github.com/psehgal0504/Final_Project/blob/master/Images/Regualtory_region_pie_chart.jpg" width="500">

## References
[A ChIP-Seq Data Analysis Pipeline Based on Bioconductor Packages](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5389943/)

[ChIPseeker: an R package for ChIP peak Annotation, Comparison and Visualization](https://www.bioconductor.org/packages/release/bioc/vignettes/ChIPseeker/inst/doc/ChIPseeker.html)
