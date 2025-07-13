## 04-04-25

Downloaded the output of the nf-core RNAseq pipeline and stored locally

Clearly issues with library complexity for all samples; see the multiQC report below

Review of multiqc

- Good coverage all samples ~ 20M or greater so standard depth
- The library sequencing is unstranded. Its a weird sequencing run
- base call quality looks very good in general
- the input fragment lengths a little short; abundance of poly-g overrperesented at the 3' end of reads
- A lot of adapter contamination at 3' end; removed which leaves the bias motif at 3' end below
- Issue possibly with library complexity; look at the dupRadar plot
- Good mapping to the exome/cds
- junction annotation: lots of novel junctions, even for standard cell-lines. Is this troubling?

Sequence bias at 3' end. Perhaps due to removal of adapter sequences at 3'end?

Only introduced after trimming, so clear adapter motif

![1743788570399](image/README/1743788570399.png)

dupRadar library complexity estimation

Expect highly expressed genes to have a lot of duplicates, but not lowly expressed genes. Possible issue with library complexity here as high percentage at low RPKM, indicating high numbers of technical duplicates

At 0.5RPKM, none of the set are below 20%; here is what a good plot looks like (for a single sample)

![1743789126126](image/README/1743789126126.png)

Good exp the relationship between duplication and expression levels should be non-linear

![1743789482445](image/README/1743789482445.png)

Read duplication; lots of both optical (similar proximity on flow cell) and non optical (pc/biological dups etc.)

The optical seems to be an issue; why are there so many? I think this is again a symptom of low library complexity; LPS_1 is an issue, but maybe we have just sequenced deep

![1743790232777](image/README/1743790232777.png)

High proportion of reads mapping to 3' exons?

![1743790542579](image/README/1743790542579.png)

Inner Distance calcualtes the insert size btween two PE reads. Negative if the freads overlap. High proportions of our reads completely overlap.

This is a very strange plot and indicates issues with the library prep/ insert size... v small proportion of our inserts (fragments) are > 400bp... I think we are sampling a very low-complexity sample. If we recover what wen want maybe ok, but big issues here

![1743790707959](image/README/1743790707959.png)

This is a good plot example.. Ours looks very poo

![1743790999789](image/README/1743790999789.png)

Alignment statistics ok: ~80% per sample, unique alignment ~75% which is good. Lots of reads not mapping as too short.

![1743789825282](image/README/1743789825282.png)
