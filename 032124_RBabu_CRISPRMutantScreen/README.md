## 03-22-24

CRISPR screen of the Tat gene
Induced mutagenesis of the Tat gene

Important question: were the sample samples run on multiple lanes  (multiplexed)?
    I guess so as the names have been merged

## To note
Reads are SE 76bp long
Each read is in the format: Krogan-RB-4588-04_S4_L004_R1_001.fastq.gz
Samplename is : Krogan-RB-4588. I guess the last number is project ID
S* this is the sample number following the order the sequences have been listed in sample sheet (1 index)
L* the lane number
R1: single end reads
001: last segment is always 001


## 03-25-24

No adapters found in the reads.. how were these removed prior to the analysis?

Combine lanes from same samples and cp data to Wynton for downstream processing


## 04-11-24
No idea why variant alleles are not matching the reference...  
first to set up docker image and mount workdir
```{r}
# mount all the projectDir to data to run the analysis
docker run -t -i -v /Users/martingordon/Documents/projects/032124_RBabu_CRISPRMutantScreen:/data ensemblorg/ensembl-vep 
```

This was the vep command used with custom reference:
All failed to map to reference...
Maybe open a help request somewhere github or biostars or something...
```{bash}
vep --input_file 090424_PrepareVEPInput_data/2024_04_11_bemaxEdits.VEP.input.tsv -o ./output/vep_out/bemax_wCustomAnno --gff ./targetGenes.gff.gz --fasta docs/targetGenes.fa --everything --tab --stats_text --check_ref --exclude_predicted --allow_non_variant
```