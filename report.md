# Assignment-2-Snakemake Workflow_ Enoch Ghosh
#Goal: To build a snakemake workflow to perform E.coli K12 sequencing analysis
## Workflow design
1. used FastQC to on forward and reverse read to check sequencing quality
2. multiqc was performed to collate all fastqc reports into a single report
3. Built an index for e.coli ref genome using Bowtie2 index
4. Alligned reads to ref genome using bowtie2 again
5. Sam to sorted bam converted the sam output from bowtie2 to a sorted BAM file
6. Samtool index was used to index the sorted Bam file for further analyses
7. Samtools flagstat was used to generate mapping statistics from sorted BAM file

Summary Report:
FastQC and MultiQC reports showed that the sequencing reads from E.coli K12  were of high quality. All 200,00 reads were primary and Qc passed reads. Mapping the reads to E.coli K12 genome resulted in 140,854 mapped reads (~70.4%) and 25,454 properly paired reads (~12.7%) with 1,250 singleton reads(~0.63%) and no secondary, supplementary and duplicated reads were detected.
While most of the reads successfully mapped to the reference genome, low proportion of propely paired reads suggests that some reads may have been imperfectly aligned. In my opinion, this could be improved through a better library preparation or alignment parameters. 
