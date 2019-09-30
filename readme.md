# INSCAPE 
INference of viral Spreaders through Computational Analysis of quasisPEcies
HCV directionality prediction software implemented in python  
Based off Pavel Skums' QUENTIN https://github.com/skumsp/quentin  
Call this program on a suspected cluster of clinical samples of viral dna for transmission network inference  
Python 3.3 code
# Prerequisites
### python modules which are not in the standard library
numpy  
scipy  
fastcluster  
six  
biopython  
networkx  
cvxopt  
pygraphviz
### other prerequisites
lsqlin.pyc (included on this github) - https://github.com/scivision/airtools/blob/master/airtools/lsqlin.py
graphviz, http://www.graphviz.org/  
mafft, http://mafft.cbrc.jp/alignment/software/  

# Usage Information

This is primarily a command line utility program. To run, type something along the lines of  

```
python inscape.py spreader.fas target.fas
```

this will run the program assuming lsqlin.py, inscape.py and the hcv fasta files are all in the current working directory. Your output (default tmp.png) should look similar to exampleout.png
For help with other options, simply type  

```
python inscape.py -h
```

If you have any questions, you can reach me at Joseph.Gussler@cdc.hhs.gov

# A note about input/output formatting
Input must be a valid FASTA file.
This program expects viral quasispecies populations (a pool of closely related mutants achieved through deep amplicon sequencing)
For each entry, your sequence ID should end with a number following the trailing underscore which denotes the frequency of that variant. For example, here we have a sequence ID with a bunch of extra information that will give the appropriate frequency of 25 for that variant

```
>P06_run12_alaska_3_2_25
```
    
# Acknowledgements
Valeriy Vishnevskiy - lsqlin.py
Pavel Skums - came up with the algorithm for QUENTIN, a precursor to INSCAPE
The rest of the DVH bioinformatics team @ CDC  
