# Supplementary-data-for-drug-response-prediction
The Supplementary data in the paper "A Survey and Systematic Assessment of Computational Methods for Drug Response Prediction"

############# GDSC_DATASET #############

Table S1. Gene expression profiles for 734 cancer cell lines and 8046 genes. The first column shows the COSMIC identifiers of the 734 cancer cell lines, and the first row shows the HGNC symbols of the 8046 genes.  

Table S2. DNA methyaltion profiles for 734 cancer cell lines and 8473 CpG loci, where each row represents a cancer cell line and each column represents a CpG locus.

Table S3. Mutation profiles for 734 cancer cell lines and 636 genes, where each row represents a cancer cell line and each column represents a gene appearing in the catalogue of Cancer Gene Census from the COSMIC database (https://cancer.sanger.ac.uk/cosmic/download, version 88), and 1 indicates mutations occur in the corresponding cell line and gene.

Table S4. Copy number variation (CNV) profiles for 734 cancer cell lines and 694 genes, where each row represents a cancer cell line and each column represents a gene appearing in the catalogue of Cancer Gene Census from the COSMIC database (https://cancer.sanger.ac.uk/cosmic/download, version 88), and 1 indicates the CNA occurs in the corresponding gene and cell line.

Table S5. The annotations of 734 cancer cell lines. The four columns are the cancer cell line names, cosmic identifiers of cancer cell lines, tissue sites which cell lines are from and histology category which cancer cell lines belong to, respectively.

Table S6. Drug response data (i.e. common logarithm of the IC50 readout) for 734 cancer cell lines and 201 drugs. The first column shows the COSMIC identifiers of the 734 cancer cell lines, and the first row shows the 201 drugs. 

Table S7. The protein--protein interaction (PPI) network involving 7136 proteins encoded by the corresponding genes from the 8046 genes appearing in the gene expression profiles. This network is extracted from the PathwayCommons database (http://www.pathway commons.org/, accessed 11 March 2019). In this table, each row represents a link in this PPI network.

Table S8. The annotations of 201 drugs. The four columns show the drug names, synonyms, drug primary targets and targeted pathways for 201 drugs, respectively. 

Table S9. Drugs' structural features. This table shows nine types of molecular fingerprints for 175 out of 201 drugs, where we did not find out the structural information for the other 26 drugs.  Each sheet records a binary matrix where each row represents a drug and each column represents a structural feature, and 1 indicates the drug presents the structural feature. 
The features with zero value across all the drugs are removed from the tables.

The description for each type of fingerprint is provided below:
SHEET NAME,	FEATURE TYPE,	DESCRIPTION
FP,	CDK fingerprint,	Fingerprint of length 1024 and search depth of 8
ExtFP,	CDK extended fingerprint,	Extends the Fingerprinter with additional bits describing ring features
EStateFP,	Estate fingerprint,	E-State fragments
GraphFP,	CDK graph only fingerprint,	Specialized version of the Fingerprinter which does not take bond orders into account
MACCSFP,	MACCS fingerprint,	MACCS keys
PubchemFP,	Pubchem fingerprint,	Pubchem fingerprint
SubFP,	Substructure fingerprint,	Presence of SMARTS Patterns for Functional Group Classification by Christian Laggner
KRFP,	Klekota-Roth fingerprint,	Presence of chemical substructures
AD2D,	2D atom pairs,	Presence of atom pairs at various topological distances


Table S10. Drug similarity matrix for 201 drugs used in the DualNets method. This is obtained by computing the Pearson's correlation between each pair of drug profiles derived from 1444 1-dimensional and 2-dimensional structural descriptors.

Table S11. 71 groups for 8046 genes in the gene expression profiles (see Table S1). 71 gene sets are selected from C2:CP subcollection and C6 collection in the molecular signatures database (MSigDB v6.2, http://software.broadinstitute.org/gsea/msigdb/collections.jsp#C2; C2:CP gene sets are canonical representations of biological processes compiled by domain experts; C6 gene sets represent signatures of cellular pathways which are often dis-regulated in cancer)  if they contain one or more primary targets of the 201 drugs. Then 8046 genes are assigned to these 71 gene sets according to whether the gene appears in the gene set or not. Genes not included in any gene set form a single group named "Others" which is not shown here.

Table S12. Drug groups. 201 drugs are classified into 23 groups, each containing drugs targeting the same pathway separated by semicolons in the second column. 

Table S13. Drug response data (i.e. the area under the drug response curve, AUC readout) for 734 cancer cell lines and 201 drugs. The first column shows the COSMIC identifiers of the 734 cancer cell lines, and the first row shows the 201 drugs.

############# CCLE_DATASET #############

Table S1 -- S13 are organized similarly with those in GDSC_DATASET.

Table S14. MicroRNA expression profiles for 385 cancer cell lines and 734 microRNAs. The first column shows the identifiers of the 385 cancer cell lines, and the first row shows the symbols of the 734 microRNAs. 

Table S15. Protein expression profiles (Reverse Phase Protein Array (RPPA) data) for 385 cancer cell lines and 214 proteins. The first column shows the identifiers of the 385 cancer cell lines, and the first row shows the antibody names. 

############# NCI60_DATASET #############                                                 

Table S1 -- S14 are organized similarly with those in CCLE_DATASET. 

Different with the GDSC and CCLE datasets, in the NCI-60 dataset, drug activity levels expressed as 50% growth-inhibitory levels (GI50). The entries in Table S6 are z-score from negative log10[GI50(molar)] data across NCI-60 for single drug.

############# CTRP_DATASET #############  
                                                  
Table S1. Gene expression profiles for 720 cancer cell lines and 7770 genes. The first column shows the COSMIC identifiers of the 720 cancer cell lines, and the first row shows the HGNC symbols of the 7770 genes.  

Table S2. Drug response data (i.e. the normalized area under the drug response curve, AUC readout) for 720 cancer cell lines and 63 drugs. The first column shows the COSMIC identifiers of the 734 cancer cell lines, and the first row shows the 63 drugs.

Table S3. The annotation of 720 cell lines in CTRP v2.1 dataset used for independent validation. The three columns are cell line names, primary tissue sites which cell lines are from and histology category which cell lines belong to, respectively.

Table S4. The common drugs between training dataset (GDSC) and testing dataset (CCLE or CTRP v2.1). The "GDSC_CCLE" (or "GDSC_CTRP") sheet provides the selected common drugs and their names in the GDSC and CCLE (or CTRP v2.1)  dataset, respectively.



Reference:
[1]  Yang, W., Soares, J, Greninger, P. Edelman, E., Lightfoot, H. et al. (2016) Genomics of Drug Sensitivity in Cancer (GDSC): a resource for therapeutic biomarker discovery in cancer cells. Nucleic Acids Research, 41, D1, 955-961.

[2] Barretina, J., Caponigro, G., Stransky, N., Venkatesan, K., Sellers, W. et al. (2012) The Cancer Cell Line Encyclopedia Enables Predictive Modelling of Anticancer Drug Sensitivity. Nature, 483, 603–607. 

[3] Ghandi, M., Huang, F., Jané-Valbuena, J., Kryukov, G., LO, C. et al. (2019) Next-generation characterization of the Cancer Cell Line Encyclopedia. Nature, 569, 503–508.

[4] Reinhold, W., Sunshine, M., Liu, H., Varma, S., Kohn, K. et al. (2012) CellMiner: a web-based suite of genomic and pharmacologic tools to explore transcript and drug patterns in the NCI-60 cell line set, Cancer research, 72, 3499-3511.

[5] Rees, M., Seashore-Ludlow, B., Cheah, J., Adams, D., Price, E. et al. (2016) Correlating chemical sensitivity and basal gene expression reveals mechanism of action. Nature Chemical Biology, 12, 109.


