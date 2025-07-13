## 06-12-25

**Overview**

Running the second set of host-viral proteins through our AF3 pipeline

Data is available through a Google Drive. Now shared to Box Folder

First check data formatting before setting up the runs

Mismatches between two proteins in the APMS set and the fasta:

```r
[1] "Brisbane_NS2" "Victoria_PA" #baits
[1] "up|N0BQ34|PB2_IBV" "up|Q596H5|PB2_IBV" #uniprot ids in fasta
```

Contact Jyoti then update jobs

**Update**

Mismatches clarified with Jyoti. Rerun the two failed samples

Looks like all the pipeline runs are failing due to an error in the pipeline; i have a version of the sandbox available, maybe regen from the singularity container incase it has been corrupted?

Try same pipeline run that worked before the shutdown on Jyotis earlier data... see if these also fail, if so raise issue on Wynton slack... I think it was using the wrong env.. set to the dev dir rather than singularity img.. check this is not the same on GitHub


## 06-16-25

Rerunning the failed and missing set on longer running jobs to avoid timeout.

So far 8/50 previously failed runs have completed successfully, continue with runs and notify Jyoti on progress.
