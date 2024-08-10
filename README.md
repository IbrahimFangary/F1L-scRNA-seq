# F1L-exploration-of-antibody-therapies-using-scRNA-from-cancer-cell-lines
analysis of scRNA seq data from cancer cell lines to explore using antibody therapies like Trastuzumab and Bevacizumab in additional cancers


# the key scientific question (KSQ)
Using available scRNA-seq data from cancer cell lines, how would you explore the use of the following FDA-approved antibody therapies in additional cancers?
- Trastuzumab: Targets HER2 and is used in the treatment of HER2-positive breast and gastric cancers.
- Bevacizumab: Targets VEGF and is used for a variety of cancers, including colorectal, lung, glioblastoma, breast, liver, and kidney cancer.

# what is meant by antibody therapies and how it works?
Antibody therapies are mainly used in targeting unwanted cells in this context it's used to target cancer cell by binding to specific markers on cancer cells or tissue 

# how does Trastuzumab work:
Trastuzumab is a monoclonal antibody against human epidermal growth factor receptor 2 (HER2) meaning that it targets cancer cells that express HER2 protein.
it acts by binding to the extracellular domain of HER2 and inhibits its homodimerization, preventing HER2-mediated signaling, It is also thought to facilitate antibody-dependent cellular cytotoxicity, leading to the death of cells that express HER2

# how does Bevacizumab work:
Bevacizumab is a monoclonal antibody against vascular endothelial growth factor (VEGF) meaning that it targets cancer cells that express VEGF protein.
VEGF helps cancer to grow blood vessels, so Bevacizumab acts by inhibiting tumor growth through multiple mechanisms including preventing the formation of new blood vessels (angiogenesis inhibition), inducing regression of newly formed vasculature and normalization of abnormal tumor blood vessels to improve cytotoxic agents’ delivery

# Why do we use scRNA data 
scRNA technology allows  us to look at the gene expression of each cell type in any heterogenous population of cells, so identifying cells and understanding their expression profile would help us see what genes specify each group of cells and target these genes, in this context identifying cancer cell subtypes and analysis of its gene expression patterns would help us to see what other cancer cells that express HER2 and VEGF proteins to target them by therapies like Bevacizumab and Trastuzumab 


# weak 2: summarizing key points in the  Kinker et al. study 
### How did the authors handle the potential caveat of co-culturing cell lines before profiling by scRNA-seq? Why do you think that caveat was or was not adequately addressed?
The authors were aware of the potential caveat that co-culturing different CCLE cell lines will introduce due to the interaction between cells which may affect expression patterns so the authors tried to test patterns of heterogeneity in co culturing and each cell line individually and they found that Co-culturing had a modest effect on average gene expression in each cell line, while patterns of heterogeneity were highly consistent between the two conditions
The co-culturing caveat was adequately addressed because the authors wanted to make sure that the heterogeneity within each cell line is due to intrinsic features of that cell line not due to the cell-cell interaction as they wanted to mimic the real complex system of cancer by modeling tumor microenvironment interactions and studying heterogeneity.
### What might be the reason why some cell lines have these discrete subpopulations while others do not?
Intra-tumoral heterogeneity is common in cancer cell lines due to differences in gene expression patterns. These differences can arise from various factors, including genetic mutations, epigenetic modifications, or environmental influences such as nutrient availability or drug exposure. Conversely, some cell lines lack intra-tumoral heterogeneity, leading to the absence of discrete subpopulations within the cancer cell line. This homogeneity is often due to a more uniform cellular environment or fewer driving mutations that reduce variability.
### What are Recurrent Heterogeneous Programs (RHPs)?
RHPs are gene expression patterns that consistently appear across different cancer cell lines and tumors, contributing to the variability observed within these cell populations.
### Why is NMF used to identify continuous variability of cellular states and how?
Non-negative matrix factorization is a dimensionally reduction method, In the context of the study, NMF is used to identify continuous variability in cellular states by decomposing the gene expression matrix into two matrices: one representing the contribution of genes to certain features such as cellular states and the other representing the activity of these features across individual cells. This decomposition helps to uncover underlying patterns in the data that correspond to different cellular states or programs that are shared across cells.
### How do the identified RHPs relate to in vivo programs of heterogeneity in tumors, and what evidence supports this relationship?
the authors examined the similarity of the in vitro RHP with the in vivo RHP and found that 7 out of the 10 cell line RHPs are highly similar to the in vivo RHPs. This is supported by overlapping The RHPs with transcriptional programs identified in patient tumors, indicating that these RHPs are relevant to real tumor biology and not merely artifacts of cell culture.



## additional Resources:
- NCI Dictionary of Cancer Terms. (n.d.). Cancer.gov. https://www.cancer.gov/publications/dictionaries/cancer-terms/def/antibody-therapy
- Johnson, K. C., Quiroga, D., Sudheendra, P., & Wesolowski, R. (2022). Treatment of small (T1mic, T1a, and T1b) node-negative HER2+ breast cancer – a review of current evidence for and against the use of anti-HER2 treatment regimens. Expert Review of Anticancer Therapy, 22(5), 505–522. https://doi.org/10.1080/14737140.2022.2063844
- Greenblatt, K., & Khaddour, K. (2024, June 22). Trastuzumab. StatPearls - NCBI Bookshelf. https://www.ncbi.nlm.nih.gov/books/NBK532246/
- Ellis, L. M. (2006). Mechanisms of action of Bevacizumab as a component of therapy for metastatic colorectal cancer. Seminars in Oncology, 33, S1–S7. https://doi.org/10.1053/j.seminoncol.2006.08.002
- Kharchenko, P.V. The triumphs and limitations of computational methods for scRNA-seq. Nat Methods 18, 723–732 (2021). https://doi.org/10.1038/s41592-021-01171-x
- Zhu, Q., Zhao, X., Zhang, Y. et al. Single cell multi-omics reveal intra-cell-line heterogeneity across human cancer cell lines. Nat Commun 14, 8170 (2023). https://doi.org/10.1038/s41467-023-43991-9
