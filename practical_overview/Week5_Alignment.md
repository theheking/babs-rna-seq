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
| Step | Description     | Command                                         | Input                                                                | Output                                          |
| ---- | --------------- | ----------------------------------------------- | -------------------------------------------------------------------- | ----------------------------------------------- |
| 1    | Genome indexing | kallisto index <--index=> <transcriptome.fa.gz> | Redference transcriptome                                             | Kallisto index (no file extension)              |
| 2    | Pseudoalignment | kallisto quant sample.fa.gz                     | FASTQ (one per run of kallisto), kallisto index (from indexing step) | abundances.h5, abundances.tsv and run_info.json |
  
  *Note: The Psuedoalignment step in the JupyterNotbook is written in a “For Loop” since we want to run it for one or more fastq files. If you have only one file, a for loop is overkill, but for more files, the For Loop is efficient since it would automatically run analysis on one file right after another. See Linux/Bash Command Line Primer for more information.

>Pseudoalignment and genomics word search
Alignment of reads is an expansive topic. Several reviews cover some of the important topics including [Stark et. al. 2019](https://www.nature.com/articles/s41576-019-0150-2). This [blog post](http://tinyheero.github.io/2015/09/02/pseudoalignments-kallisto.html) and the (kallisto paper)[https://www.nature.com/articles/nbt.3519] are required readings to get a deep understanding of the subject.

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

>CUSVFVMAASJFHUTMNCCQMBVXOLBEETYHSRBWOSEY
>MOBJEYXAZMPMFENZHQKMHHSCZUXUQYEBQONJVYWH
>LCMIFVSPNMAGIJAOOFCWNYYDETTLMGCDOBSLOPXO
>ZAUSKOGLCYOIKIXZSHOXHLYGZJLRLZMRGHRFRJWN
>HBEOJQLIXUYAIAWMJASRBOVSBHMAHJFPUOXTQIYZ
>LSSCVOGPJCIIMUILZCFKLASLFLQFIZVSYXWJYNMJ
>QPWLYGLRTSTQHYUVFVGGPDMICLGDUMZOVPHFPLOD
>YFZAYPVONRRCPHJPNJVROZEZPBLZNYBQHOVUPOGJ
>SAVCNZWIYQKHJOLKQBHZYGJZKUEHKJLCLXOLMUJF
>YJAGKRFQOQRNAXXXZAZUMMWMLKWNREHDFOLVVYWK
>ATOXWLBGQECNAMWJIMONGSAVKGSHUVUOROVJRJGT
>AJLVEYWLSFPUIYABELQZLYLUGZJGPGWEVPXYCHGO
>IPXOCIPREEDCYTFZHBDTTOIJRWLEYEMMTRIDSMGJ
>BNEZKUNVOXZFIXAAGGYUWAYZSNVUHXJZMMPXBPTE
>QMVXMUJAFUGBBLAVVCGVBDIGDBIDBSHTEVPCJTUB
>ELJIPXDVTMPNCROAPIHZMROJXZFCDHRYWIEUSZST
>ERRCPCLAPIJROAAUKZNDYYKNWKNUNFDKSTLYTXKA
>UAMNKGZVKWMOYGLLWUJOECUNBRUGRPWWUNNVEXYF
>MQYPHTEPNKPLWECXVORINUEHHVLVBNFUJJXNEZYT
>MJDQTZMIRJXMLYUCXYCVFQHHQBERSMGQLRWNYAJP
>IELYQQDAIXJDTUONASHBTLCZISHQWCMJZFAFJOXE
>UGZWMJGDLLRKIZVVLPHYBCULVCAIRMMEQPRRHFHQ
>FFCWSFSQZJTBCVFHUAEECJPXKHMKRKJFBZVQNOMZ
>ZZZEMQQNVWUXDOYBDHSDFLHMAQEWFKWPMIGJVZUT
>ZNEQDNAHXMPBLRVDEBJRJFTDOIWUPFLSIYOOHNQH
>TTMIXMVUMETGMJWFEWCRITKZWZGVMCNQRAPDCJZD
>AXPTCGYNKVFDPALHRQNPKQUBSEGOOQCVUDDHTIWR
>GEMJXKJGSSRAROGDWETVVTZMWUSCYXIKTUFLUIXO
>BDZFSFRPFXHALCKUGTOHGMEHYPRPTFXUSWSKDBWC
>UGGJXCDKYYZZFLDAWLDYJLCRSTDSMLOGPCVAUDZZ
>AHGKHDAGOHYQDKGWDTOGFVOSRKJCPRRENRQRBBPQ
>ABHWPOFZYTGHXPREABCTWABQLZLYBOQVHOMUHGRS
>FPNWCEQGTYJEDRWAVDYKUAZMLVVNTYNRZHPFHYGR
>UAJNXZWZSBLEVYIGLRPFNZLOGRULAHIAHDLXTJXF
>DQEKRQNVJACCBVGABSKTWRPYEFXNEHSICVLHWOIV
>GVOGZWUSLGRGHMVENEYNSBCZRLOZYCMXCYGWUMSG
>LFXDWDWHJYXAXDVWVMTPKQVTAYHNCADYJCNKNDZM
>ASJBGHYSPRUIIVQDAVUQBEEDNQKBKQPMKYQKRIKV
>MWFHPISMEIUIVZVBEUKTFOUADMUDXAJSGYHLXUSP
>OSIVVLZMDTLDMCLGZLEGWLPVPWOLNERAINTAESFR
 
Pseudoalignment is one approach to this computational “word search”. It takes advantage of a trick to speed up performance without loosing accuracy. Take the second line in our “DNA” word search puzzle:

>MOBJEYXAZMPMFENZHQKMHHSCZUXUQYEBQONJVYWH

There is no “D” in this line. True, We don’t know that until we read the entire line, but once we realize this line can’t possible be a match without a “D” We can ignore this line. Word search puzzles don’t have to be read in just one direction (words might be on diagonals, backwards, etc.), but now consider what happens in the pseudoalignment “word search”. In this case we are searching not the entire genome, but linear transcripts:


>Transcript 1: CUSVFVMAASJFHUTMNCCQMBVXOLBEETYHSRBWOSEY
>Transcript 2: MOBJEYXAZMPMFENZHQKMHHSCZUXUQYEBQONJVYWH
>Transcript 3: LCMIFVSPNMAGIJAOOFCWNYYDETTLMGCDOBSLOPXO
>Transcript 4: ZAUSKOGLCYOIKIXZSHOXHLYGZJLRLZMRGHRFRJWN
>Transcript 5: ZNEQDNAHXMPBLRVDEBJRJFTDOIWUPFLSIYOOHNQH

We can immediately eliminate transcripts that don’t contain the letter D:

>Transcript 3: LCMIFVSPNMAGIJAOOFCWNYYDETTLMGCDOBSLOPXO
>Transcript 4:
>Transcript 5: ZNEQDNAHXMPBLRVDEBJRJFTDOIWUPFLSIYOOHNQH


Immediately, the problem is made easier by throwing away transcripts that could not contain the answer. This is not an exact analogy but basically, rather than trying to match every read to every position in the genome, Kallisto is faster because 1) we are only matching to the transcriptome (a subset of the genome) and 2) we focus only on transcripts that could have generated a particular read.


> Note
Pseudoalignment is just one approach to aligning RNA-Seq reads. Other software will do full alignments of the read to a transcriptome or genome. These methods have different advantages and requirements.


There are a few files we need to analyze our data with Kallisto

- Reference transcriptome: A file of all the known trasncripts of the mouse genome
- Reference annotations: A file with information on the location and structure of the genes in the mouse genome
These data (for mouse, and many other organisims) are available from public databases
  
  
> Obtain the reference data

Index transcriptome
We will now use Kallisto's indexing function to prepare the transcriptome for analysis. The "Index" is a lookup table for the transcriptome that allows it to be more easily searched by Kallisto. First let's organize our files by creating a new directory to hold our kallisto work.

mkdir -p /home/gea_user/rna-seq-project/kallisto
Next run the indexing command. This prepares the transcriptome so that we can peudoalign reads to it.

kallisto index --index="Mus_musculus.GRCm38_index" /home/gea_user/rna-seq-project/transcriptome/Mus_musculus.GRCm38.cdna.all.fa.gz
We now have a transcriptome index which can now be used for pseudoalignment, we'll move it into the transcriptome folder:

mv Mus_musculus.GRCm38_index /home/gea_user/rna-seq-project/transcriptome/
We also will need the mouse GTF file, a file containing coordinates and descriptions for all gene names and locations - we will also download this from Ensembl.

wget ftp://ftp.ensembl.org/pub/release-97/gtf/mus_musculus/Mus_musculus.GRCm38.97.chr.gtf.gz
We will make a folder called annotations and save that there as well.

mkdir -p /home/gea_user/rna-seq-project/kallisto/annotations
mv Mus_musculus.GRCm38.97.chr.gtf.gz /home/gea_user/rna-seq-project/kallisto/annotations
Finally we also need a textfile that has the name of each mouse chromosome (e.g. 1, 2, 3, ... X, Y, MT) and the length of each chromosome, This will be used for visualization. The information will be downloaded and then edited using bash commands.

wget ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/001/635/GCF_000001635.26_GRCm38.p6/GCF_000001635.26_GRCm38.p6_assembly_report.txt
head -n64 GCF_000001635.26_GRCm38.p6_assembly_report.txt|tail -n21|cut -f1,9 > /home/gea_user/rna-seq-project/kallisto/annotations/mouse_chromosomes.tsv
We can see this edited list of chromosome numbers and lengths here:

cat /home/gea_user/rna-seq-project/kallisto/annotations/mouse_chromosomes.tsv
Quantify reads
In this final step, we will run Kallisto on all of our files to quantify the reads. We will write a for loop to do this. Let's see once again our trimmed reads

Exercise 3: Pseudoaligning reads with Kallisto
Working with data you trimmed yourself
If you used trimmomatic to trim your reads, run the next cell (otherwise skip to the cell for fastp reads)

cd /home/gea_user/rna-seq-project/trimmed-reads
ls
We don't want the small_trimmed.fastq.gz file to be part of our analysis, so we will delete it

rm small_trimmed.fastq.gz
Now we should have just the trimmed file(s) we want to analyze.

ls
Working with data pre-trimmed data
All instructions for the commands we are using are in the Kallisto manual: https://pachterlab.github.io/kallisto/manual. Since we are using single read data, we need to provide information on the fragment length used for the library (200) and an estimate of the standard deviation for this value - here we will have to guess (20). We need to run Kallisto separately on each of our 6 files so we will use a for loop.

for file in *_trimmed.fastq.gz; do output=$(basename --suffix=.fastq.gz_trimmed.fastq.gz $file)_quant; kallisto quant\
 --single\
 --threads=8\
 --index=/home/gea_user/rna-seq-project/transcriptome/Mus_musculus.GRCm38_index\
 --bootstrap-samples=25\
 --fragment-length=200\
 --sd=20\
 --output-dir=$output\
 --genomebam\
 --gtf=/home/gea_user/rna-seq-project/kallisto/annotations/Mus_musculus.GRCm38.97.chr.gtf.gz\
 --chromosomes=/home/gea_user/rna-seq-project/kallisto/annotations/mouse_chromosomes.tsv\
 $file; done
Lets move our results to an appropriate directory and view the directories containing our analyses:

mkdir -p /home/gea_user/rna-seq-project/kallisto/analyzed
mv *_quant /home/gea_user/rna-seq-project/kallisto/analyzed
cd /home/gea_user/rna-seq-project/kallisto/analyzed
ls
Each of these directories containes several files, lets remind ourselves what each of these directories contain:

SRA Sample	Sample Name	Folder Name
SRS1794108	High-Fat Diet Control 1	SRR5017135_trimmed.fastq.gz_quant
SRS1794110	High-Fat Diet Control 2	SRR5017137_trimmed.fastq.gz_quant
SRS1794106	High-Fat Diet Control 3	SRR5017133_trimmed.fastq.gz_quant
SRS1794105	High-Fat Diet Tumor 1	SRR5017132_trimmed.fastq.gz_quant
SRS1794101	High-Fat Diet Tumor 2	SRR5017128_trimmed.fastq.gz_quant
SRS1794111	High-Fat Diet Tumor 3	SRR5017138_trimmed.fastq.gz_quant
Let's look at the files in the High-Fat Diet Control 1

cd /home/gea_user/rna-seq-project/kallisto/analyzed/SRR5017135_trimmed.fastq.gz_quant
ls
This file contains a list of abundances (counts) for the Regular Diet Control sequences from SRR5017139

head -n 100 abundance.tsv
  
  

  
  
  
  
  
