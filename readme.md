# PYCIVO 
Primary case inference in viral outbreaks through analysis of intra-host variant population
HCV outbreak source attribution software implemented in python  
Based off Pavel Skums' QUENTIN https://github.com/skumsp/quentin  
Call this program on a suspected cluster of clinical samples of viral dna for transmission network inference  

## Requirements
Install necessary requirements for minimal text output with the following

```
pip install -r requirements.txt
```

Additionally, If you would like to use the -a option, you have to have mafft installed

http://mafft.cbrc.jp/alignment/software/  

If you want to infer the entire network, the network is output using graphviz

graphviz, http://www.graphviz.org/  

You also must install the pygraphviz python module for this to work

The output will look similar to exampleout.png
# Usage Information

To run, type the following into a console:  

```
python pycivo.py primary_case.fas target.fas
```

The software will output to stdout as well as the output file (default PYCIVO_OUTPUT.txt) 
For help with other options, simply type  

```
python PYCIVO.py -h
```

If you have any questions, you can reach me at Joseph.Gussler@cdc.hhs.gov

# A note about input/output formatting
Input must be a valid FASTA file with some extra specifications. The software expects a multiple sequence alignment of populations of viral quasispecies achieved through deep amplicon sequencing. For each entry in each FASTA file, the ID line should display the frequency following the last underscore. For example, here is a correctly formatted sequence ID with an associated frequency of 25. 
```
>P06_run12_alaska_3_2_25
```

# Acknowledgements
Valeriy Vishnevskiy - lsqlin.py
Pavel Skums - devised the network inference algorithm QUENTIN 
The rest of the DVH bioinformatics team @ CDC  