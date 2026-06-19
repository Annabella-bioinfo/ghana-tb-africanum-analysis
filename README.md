\# Genomic Sequence Analysis of \*M. africanum\* Clinical Isolates from Ghana



\## Overview

\*Mycobacterium africanum\* accounts for approximately 20% of TB cases in Ghana 

and up to 40-50% in some other West African countries, yet it remains less 

studied than \*M. tuberculosis\*. Understanding the genetic diversity of local 

clinical isolates matters for drug resistance surveillance — particularly in 

the rpoB gene, where mutations drive resistance to rifampicin, a first-line 

TB drug.



This project uses Python and Biopython to analyze rpoB and hsp65 gene sequences 

from \*M. africanum\* isolates collected from Ghanaian TB patients. The sequences 

were first characterized using NCBI BLAST, then explored programmatically to 

calculate GC content, check data quality, and quantify inter-strain genetic 

differences.



\## Data Source

\- 4 partial gene sequences from NCBI GenBank (accessions FJ617583-FJ617586)

\- Organism: \*Mycobacterium tuberculosis\* variant africanum

\- Source: Human sputum samples, Ghana

\- Reference: Goncalves Vasconcellos et al. — distinct genotypic profiles of 

&#x20; \*M. africanum\* clades causing tuberculosis in Ghana



\## Tools Used

\- Python 3.13

\- Biopython (SeqIO, SeqUtils)

\- Matplotlib

\- Jupyter Notebook

\- NCBI BLAST (sequence characterization)



\## Analysis

The notebook covers:

1\. Loading and verifying FASTA sequences

2\. GC content calculation and visualization

3\. Sequence quality check (ambiguous base count)

4\. Pairwise SNP comparison between Ghanaian strains

5\. Heatmap visualization of inter-strain differences



\## Key Findings

\- All sequences have GC content between 62-64%, consistent with the known 

&#x20; high-GC signature of the \*M. tuberculosis\* complex

\- No ambiguous bases found; all four sequences are clean and suitable 

&#x20; for analysis

\- Two SNP positions identified at positions 166 and 280 across the three 

&#x20; rpoB strains

\- FJ617585 and FJ617584 are the most divergent pair (2 SNPs apart), while 

&#x20; FJ617586 sits between them with 1 SNP difference from each

\- This pattern suggests at least two distinct rpoB lineages of \*M. africanum\* 

&#x20; are circulating in Ghana — one matching the global majority sequence and 

&#x20; one carrying local variants. If either SNP falls within the rifampicin 

&#x20; resistance-determining region (RRDR), it could have direct implications 

&#x20; for TB treatment outcomes in Ghana



\## How to Run

1\. Clone this repository

2\. Install dependencies: pip install biopython matplotlib

3\. Open ghana\_tb\_sequences\_analysis.ipynb in Jupyter

4\. Run all cells in order



\## References

\- Asante-Poku A, Yeboah-Manu D, Otchere ID, Aboagye SY, Stucki D, 

&#x20; Hattendorf J, et al. (2015) \*Mycobacterium africanum\* Is Associated with 

&#x20; Patient Ethnicity in Ghana. PLoS Negl Trop Dis 9(1): e3370. 

&#x20; https://doi.org/10.1371/journal.pntd.0003370

\- Goncalves Vasconcellos SE et al. Distinct genotypic profiles of the two 

&#x20; major clades of \*Mycobacterium africanum\* causing tuberculosis in Ghana. 

&#x20; Submitted 2009. NCBI GenBank accessions FJ617583-FJ617586.



