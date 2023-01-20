---
layout: page
title: Week 5 Alignment with Kallisto 
---


=====================

> Overview


Despite these challenges, RNA-Seq is a very useful experiment and researchers have worked through many of the challenges above to develop software that can help us infer what is happening in the transcriptome.

Kallisto is a quick, highly-efficient software for quantifying transcript abundances in an RNA-Seq experiment. Even on a typical laptop, Kallisto can quantify 30 million reads in less than 3 minutes.

In order to analyze data with Kallisto we need several inputs:

We need the FastQ files from the RNA-Seq experiment; we usually start with reads that have already been trimmed/filtered
We need a reference transcriptome. This is a file that has the sequences for all the known expressed genes. Reference transcriptomes are usually available from repositories like Ensembl and NCBI. We will be using the mouse reference transcriptome (available on the linked page “Download sequences in FASTA format for transcript”). Unlike a genome, the transcriptome is only coding genes.




>Optional

We also will get the annotations and chromosome information for our subsequent visualization steps:

We need a reference annotations. This is a file that has the names and locations for all the genes in the transcriptome. Annotations have information like how many introns/exons a gene contains, and perhaps other information about the gene (such as a predicted function). This information also comes from the Ensembl page
Because of the way we sequenced (single-end sequencing) we also need to know the chromosome lengths and this information from the NCBI mouse reference page.
Basic Kallisto Steps

Analysis with Kallisto has two main steps (see the manual on the Kallisto home page):
 Outer pipes  Cell padding 
No sorting
| Step | Description       | Command                                                                                                                                                                                                                                     | Command explanation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Input                                                                            | Output                             |
| ---- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ---------------------------------- |
| 1    | Genome indexing   | kallisto index <--index\=\> <transcriptome.fa.gz>                                                                                                                                                                                           | *   kallisto index: Command to begin the indexing
*   –index=: The name your want your index file to be called
*   transcriptome.fa.gz: A transcriptome in fasta format (may becompressed “.gz”)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Reference transcriptome                                                          | Kallisto index (no file extension) |
| 2    | Pseudoalignment\* | kallisto quant
--single
--threads\=<t>
--index\=<index name>
--bootstrap-samples\=<b>
--fragment-length\=<f>
--sd\=<s>
--output-dir\=<dir>
--genomebam
--gtf\=<annotations.gff>
--chromosomes\=<chromosome_list.tsv>
<fastq_input.fastq.gz> | *   kallisto quant: Command to start Kallisto
*   single: Indicates this is single-end sequence data
*   threads=[t]: Optional - indicates how many CPU threads to use
*   bootstrap-samples=<b>: Conduct <b> (integer) of bootstrap samplings
*   fragment-length=<f>: Estimated average fragment length the
    
    sequencing library used DNA fragments of length f (integer)
    
*   sd=<s>: Estimated standard deviation of fragment length
    
    (default: -l, -s values are estimated from paired end data, but are required when using –single)
    
*   output-dir=<dir>: Name of directory where results should be output
*   genomebam: Create a pseudobam file (will be used in visualization)
    
    to see where individual reads map on the genome
    
*   gtf=<annotations.gff>:GTF file for transcriptome annotation information
    
    (required for –genomebam)
    
*   chromosomes=<chromosome_list.tsv>: Tab separated file with
    
    chromosome names and lengths (optional for –genomebam, but recommended)
    
*   <fastq_input.fastq.gz>: FastQ file for analysis | *   FastQ file (one per run of Kallisto)
*   Kallisto index (from indexing step) |

  
  *Note: The Psuedoalignment step in the JupyterNotbook is written in a “For Loop” since we want to run it for one or more fastq files. If you have only one file, a for loop is overkill, but for more files, the For Loop is efficient since it would automatically run analysis on one file right after another. See Linux/Bash Command Line Primer for more information.

>Pseudoalignment and genomics word search
Alignment of reads is an expansive topic. Several reviews cover some of the important topics including Stark et. al. 2019. This blog post and the kallisto paper are required readings to get a deep understanding of the subject.

To try and reduce this problem to its most basic, let’s use an analogy. In the traditional case, when software does alignment, it tries to match a read to the genome.
  
  
  
  
> Genome: ACTACGTAGCCGTCAAATATCCCGGGTATCGTACGATCGACGT
>
> Read:   AAATTTCCCGGG
  
If we move things around we can find the match:


> Genome: ACTACGTAGCCGTCAAATATCCCGGGTATCGTACGATCGACGT
>                    |||| |||||||
> Read:              AAATTTCCCGGG
  
 
  
In this example a “|” appears when there is a match, and we have one mismatch. Although finding this match was simple, the genome is far more complex.

In the word search below is the word “DNA”. Can you find it? It may take you a while. Searching for words is a process similar to taking sequencing reads and trying to match them to the genome. Computers are fast, but just as matching a small word (3 letters) in a large (1639 letter) word puzzle is time-intensive, it take a long time to match millions of short reads against genomes of billions of nucleotides.


 
  
There are a few files we need to analyze our data with Kallisto

- Reference transcriptome: A file of all the known trasncripts of the mouse genome
- Reference annotations: A file with information on the location and structure of the genes in the mouse genome
These data (for mouse, and many other organisims) are available from public databases
  
  
  

  
  
  
  
  
