# Poster SIB days

## Methods
1. Hierarchical clustering of STRING generates functional clusters for > 5000 organisms

We used HPC-clust [1] to perform average linkage hierarchical clustering of the STRING v11 protein-protein association networks of all 5090 organisms, using (1 - STRING score) as as the distance between protein pairs. 
All hierarchical clusters where retained, but simplified to require a difference of at least 5 proteins between each parent and child cluster.
Clusters where automatically named by calculating their overlap with existing annotations and incorporating the annotation if the cluster was closely matching an existing annotation term. 
We further disregarded all clusters larger than 200 proteins in order to reduce redundancy and to keep results specific. In the following, these hierarchical clusters will simply be called STRING clusters.
  
2. STRING clusters detect more functional associations than GO in understudied species based on > 3000 datasets

We used more than 3000 community-provided experimental datasets from 60 organisms to perform functional enrichment analysis on, using the STRING Functional Enrichment Analysis functionality [2], accessible at string-db.org > Proteins with Values/Ranks. 
Among others, we enriched for functional sets and pathways from GO Biological Process, Reactome, UniProt, and KEGG. The figure shows the total number of all significant terms across all datasets, for each species and annotation database. We found that while yielding comparable significance levels and effect sizes, STRING clusters provide the highest number of enriched terms amongst the pathway databases.    


3. STRING clusters provide superior coverage of human proteome

The GO Biological Process, Reactome, UniProt, and KEGG terms were compared to STRING clusters by counting the number of times each human protein-coding gene appeared in each database. STRING clusters and UniProt keywords covered the vast majority of the proteome with three or more annotations per protein, while two-thirds of the proteome are completely missing from KEGG.


[1] Matias Rodrigues, J. F., & Von Mering, C. (2014). HPC-CLUST: Distributed hierarchical clustering for large sets of nucleotide sequences. Bioinformatics, 30(2), 287–288. https://doi.org/10.1093/bioinformatics/btt657
[2] Szklarczyk, D., Gable, A. L., Lyon, D., Junge, A., Wyder, S., Huerta-Cepas, J., … von Mering, C. (2018). STRING v11: protein–protein association networks with increased coverage, supporting functional discovery in genome-wide experimental datasets. Nucleic Acids Research, 1–7. https://doi.org/10.1093/nar/gky1131

