# correct_bacode.py
[![DOI](https://zenodo.org/badge/114735129.svg)](https://zenodo.org/badge/latestdoi/114735129)

The command is correction of cell barcoding containing RT primer sets for Quartz-Seq2 which one of a high throughput single-cell RNA-sequencing [1]. The cell barcdes of Quartz-Seq2 are designed such that the minimum Sequence–Levenshtein distance between two sequences should be greater than 5, which leads to the correction of two nucleotides of mismatch, insertion and deletion in sequence reads [2]. The program can correct cell barcode if sequence error are occured.

1. [Sasagawa Y et al. Quartz-Seq2: a high-throughput single-cell RNA-sequencing method that effectively uses limited sequence reads](https://www.biorxiv.org/content/early/2017/07/21/159384)
2. [Buschmann T. DNABarcodes: an R package for the systematic construction of DNA sample tags. Bioinformatics. 2017;:btw759.](https://academic.oup.com/bioinformatics/article/33/6/920/2804018)

## Requirements
* R
  * [DNABarcodes](https://bioconductor.org/packages/release/bioc/html/DNABarcodes.html)
* Python 2.7
  * numpy==1.11.0
  * pandas==0.18.0
  * pyper==1.1.2
  * pysam==0.9.0
  * seaborn==0.7.0

## Usage
```
correct_barcode.py

Usage:
    correct_barcode.py (-i input_file) (-b barcode_file) (-o output_file) (-m metric) (-d distance)
    correct_barcode.py -h | --help
    correct_barcode.py -v | --version

Options:
    -i input_file       Bam file resulted of TagReadWithGeneExon
    -b barcode_file     Single-column file for designed barcode (No header)
    -o output_file      Bam file name for output of this program
    -m metric           The distance metric to be used. (seqlev or hamming)
    -d distance         Distance for error correction
    -h --help           Show this screen
    -v --version        Show version
```

## Lisense
[MIT](https://raw.githubusercontent.com/rikenbit/correct_barcode/master/LICENSE)
