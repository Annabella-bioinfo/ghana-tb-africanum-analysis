# BLAST Analysis of *Mycobacterium africanum* rpoB and hsp65 Gene Sequences from Ghana

## Background

*Mycobacterium africanum* accounts for approximately 20% of TB cases in Ghana and up to 40–50% in some other West African countries. As a member of the *M. tuberculosis* complex, it is an important yet understudied cause of tuberculosis in West Africa. Understanding the genetic diversity of clinical isolates from Ghana is relevant to both surveillance and drug resistance monitoring — particularly in the rpoB gene, where mutations drive resistance to rifampicin, a first-line TB drug.

This analysis used four partial gene sequences deposited in NCBI GenBank — three rpoB sequences and one hsp65 sequence — all derived from *M. africanum* clinical isolates collected from Ghanaian TB patients. The sequences were sourced from a study on the distinct genotypic profiles of *M. africanum* clades causing tuberculosis in Ghana (Goncalves Vasconcellos SE et al., submitted 2009). BLAST was used to compare each sequence against the global nucleotide collection (nr/nt) to assess conservation, identify SNPs, and evaluate potential drug resistance implications. This analysis forms Part 1 of a two-part project; Part 2 involves computational sequence analysis using Python and Biopython, where SNP positions identified here were confirmed programmatically.

## Sequences Analysed

| Accession | Gene | Organism | Source |
|-----------|------|----------|--------|
| FJ617586 | rpoB | *M. tuberculosis* variant africanum | Human sputum, Ghana |
| FJ617585 | rpoB | *M. tuberculosis* variant africanum | Human sputum, Ghana |
| FJ617584 | rpoB | *M. tuberculosis* variant africanum | Human sputum, Ghana |
| FJ617583 | hsp65 | *M. tuberculosis* variant africanum | Human sputum, Ghana |

## BLAST Results Summary

| Accession | Gene | Top Hit | Identity Scores | Mismatches |
|-----------|------|---------|-----------------|------------|
| FJ617586 | rpoB | *M. tb* strain N1202 | 100% (5), 99.72% (95) | SNP pos 280 (T→C) |
| FJ617585 | rpoB | *M. tb* isolate CCS_G1826m3 | 100% (100) | None |
| FJ617584 | rpoB | *M. tb* strain N1202 | 100% (5), 99.72% (5), 99.44% (80) | 99.72%: SNP pos 166 (T→C); 99.44%: SNP pos 166 (T→C) + SNP pos 280 (T→C) |
| FJ617583 | hsp65 | *M. tb* isolate CCS_G1826m3 | 100% (9), 99.77% (91) | SNP pos 396 (G→C) |

## Key Observations

**High sequence conservation.** All four sequences matched global *M. tuberculosis* complex sequences with identities above 99.7%, confirming that both rpoB and hsp65 are highly conserved across the TB complex regardless of geographic origin. This is expected for genes that perform critical cellular functions — mutations tend to be lethal, so the sequence stays stable across strains and species.

**Recurring SNP at position 280.** A T→C substitution at position 280 of rpoB appeared in two of the three Ghanaian rpoB sequences (FJ617586 and FJ617584). The same substitution also appears in the majority of near-identical global hits, suggesting this is not random variation. When the same change recurs independently across geographically diverse strains, it is consistent with positive selection pressure — strains carrying this substitution may have a survival advantage under rifampicin treatment, allowing them to persist and spread.

**Inter-strain variation within Ghana.** FJ617585 matched global sequences at 100% across all 100 hits, while FJ617586 carried a SNP at position 280. Both strains were isolated from Ghanaian patients in the same study, yet they differ from each other at the sequence level. This indicates at least two distinct rpoB variants of *M. africanum* are circulating in Ghana — one matching the global majority sequence and one carrying the T→C substitution at position 280.

**FJ617584 carries two SNPs.** This sequence showed the highest divergence, with SNPs at both position 166 and position 280. The 99.44% identity group (80 hits) carries both substitutions, while the 99.72% group (5 hits) carries only the position 166 change. This pattern suggests FJ617584 may represent a more divergent sub-lineage within the Ghanaian *M. africanum* population — one that acquired the position 166 mutation independently of the position 280 change seen in FJ617586.

## Drug Resistance Implications

The rpoB gene encodes the beta subunit of RNA polymerase, which is the binding target of rifampicin. Resistance to rifampicin almost always arises from mutations within an 81 base pair stretch of rpoB called the rifampicin resistance determining region (RRDR), spanning codons 426–452. The WHO catalogue of *M. tuberculosis* complex mutations identifies codons 450, 445, 435, 452, and 430 as the most clinically significant resistance sites.

The SNPs identified in this analysis — at nucleotide positions 166 and 280 of the partial sequences — could not be directly cross-referenced against the WHO catalogue without first mapping these positions to their corresponding codon numbers in the full rpoB gene. This requires translating the partial sequence in the correct reading frame and aligning it against a complete reference sequence. Whether positions 166 and 280 fall within the RRDR (codons 426–452) is therefore unconfirmed and represents a clear next step. If either SNP maps to a known resistance codon and causes a non-synonymous amino acid change, it would have direct implications for rifampicin susceptibility testing in Ghanaian TB patients.

## Conclusion

BLAST analysis of four *M. africanum* sequences from Ghana confirmed strong conservation of both rpoB and hsp65 genes across the global *M. tuberculosis* complex. Three SNPs were identified — at positions 166, 280, and 396. The position 280 T→C substitution in rpoB was the most notable finding: it appeared in two of the three Ghanaian strains and in the majority of near-identical global hits, consistent with positive selection pressure. The inter-strain variation observed across all three Ghanaian rpoB sequences suggests the local *M. africanum* population is not genetically uniform, with implications for TB drug resistance surveillance in Ghana. SNP positions identified here were subsequently confirmed using Python-based sequence comparison in Part 2 of this project.

## References

- Asante-Poku A, Yeboah-Manu D, Otchere ID, Aboagye SY, Stucki D, Hattendorf J, et al. (2015) *Mycobacterium africanum* Is Associated with Patient Ethnicity in Ghana. PLoS Negl Trop Dis 9(1): e3370. https://doi.org/10.1371/journal.pntd.0003370
- Goncalves Vasconcellos SE et al. Distinct genotypic profiles of the two major clades of *Mycobacterium africanum* causing tuberculosis in Ghana. Submitted 2009. NCBI GenBank accessions FJ617583–FJ617586.
- World Health Organization (2022). WHO catalogue of mutations in *Mycobacterium tuberculosis* complex and their association with drug resistance.
