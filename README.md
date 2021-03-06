# Tmapper
Mapping T-DNA insertions in Arabidopsis with NGS sequence data.  
Author: Keegan Leckie


Agrobacterium mediated transformation of Arabidopsis is commonly used in the creation of transgenic Arabidopsis plants. Using NGS sequencing data from your transgenic line, Tmapper takes FASTQ format sequencing data, your insert sequence in FASTA format along with the TAIR genome and GFF3 reference files, to map the position of your T-DNA insertion within the Arabidopsis genome.

dependencies:  blastall, formatdb, bash environment

````
usage: TMapper -a <read1.fastq> -b <read2.fastq> -i <insert.fasta> -f <genome.fasta> -g <genome.gff3> -lprdh

Arguments:

-a	<read1.fastq> 		sequencing reads (read 1 if paired-end):	Fastq format <br>
-b	<read2.fastq> 		read 2 of paired-end(optional):			Fastq format <br>
-i	<insert.fasta> 		T-DNA insert sequence:				Fasta format <br>
-f	<genome.fasta>  	Organism genome sequence:			Fasta format(clean) <br>
-g	<genome.gff3> 		General Feature Format(.GFF3)(optional):	GFF3 format <br>


Flags:

-l 		Turn on insert loci mapping (requires pair-end reads)<br>
-p		Provide file of processed reads in fasta format<br>
-r		Provide files of reads mapping to T-DNA insert and mapping positions<br>
-d		Convert border spanning reads to .bed files<br>
-h		Extended usage message<br>

````