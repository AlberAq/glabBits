## Read-depth Script

The script uses two inputs:
1) A BED file conatining start and end positions of each polyorphic deletion reported in the 1000 Genomes dataset.Let us call this del-BED 
2) A BAM file downloaded from a repository such as http://cdna.eva.mpg.de/neandertal/altai/AltaiNeandertal/bam/.

The script performs the following operations:
1) The input BAM file is converted into a BED file that contains the start and end positions of each read. Let us call this read-BED.
2) Read-bed and del-BED are compared against each other. The number of reads, associated with the input file, that overlaps the length of each deletion are counted.

The script produces the following output:
1) File containing conatining the start and end positions of each deletion, and an added column with the numbers of reads (associated with the input file) intersecting with each deletion.







## Required Libs

```
python/py37-anaconda-2019.03
bedtools/2.23.0
```
