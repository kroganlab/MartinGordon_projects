## 01-02-25

For now, as I have no access to the data on C3PO, just take the merged counts table and go from there
Redo the PW comparisons; normalize using MAGECK during the testing (or can provide our own normalization) and regenerate the volcanoplots
Other visualizations? Heatmaps? Pairwise correlations of normalized counts? Look at similar publications to see what to generate

Have run the PW comparisons using sgControl normalization; look at the outputs and see if we find the same hits upregulated with the shared document
Didnt find any genes differentially expressed between the conditions... need to consider a different normalization approach

Issues with the normalization in AP analysis, so restarting from the concatenated reads
Will use bowtie to build a reference from the library fasta AP provided, then will align the reads to the reference to count for each of the samples
First need to use cutadapt or some other trimming tool to remove 5' and 3' adapters... check out the files first to familiarise myself with the format