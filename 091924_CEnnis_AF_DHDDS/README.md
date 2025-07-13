# 09-23-24

First ran an alignment of the DHDDS sequences
First thing to note; the human (isoform1) and yeast sequences & structure are quite divergent
This is (probably?) good news as the inference is not simply based on the yeast?


**notes**
After superimposing the 5 structures, no difference in their alignments

r205c is in a beta sheet position
Next, we want to align each of the mutants vs the reference (isofrom1) as the backbone


Colored all mutations
- 37 is dark red; in alpha-helix
- 205 is purple; beta-sheet
- 211 is green; disordered region? plddt still scores high

Other interesting thing is they are all located in high scoring regions and pretty close together in the final structure

realigned giving more weight to secondary structure and increasing BLOSUM matrix, but no impact on output...


Thermo_MPNN
No evidence of mutations impacting thermostability
Not so sure about my approach here... is it a little circular? Feeding AF models into a sequence from structure prediction tool to assess SNP impact on thermostability?
Instead look at the PDB structure in the tool and lets see how the mutations impact that

# 09-24-24
DHDDS and NgBR (NUS1 in yeast) form a complex that plays an important role in N-linked glycosylation
NgBR/NUS1 stabilizes DHDDS through dimerization, participates in the enzyme’s active site through its C-terminal -RXG- motif
205,211 on DHDDS are binding sites for Isopentenyl diphosphate (IPP) (universal precursor for carotenoids synthesized from glucose)

Questions
What is the cis-PTase catayltic core domain highlighted in the DHDDS_NgBR_complex.rot1.png plots