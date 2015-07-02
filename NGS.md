# NGS

## If you already have VCF files:

1. Quality control, a good post about it:
* http://www.cureffi.org/2012/10/17/descriptive-statistics-and-quality-control-on-variants/

2. Annotate, manipulate, query variants using Variant tools (vtools)
* Can also perform association. Good tutorial on quality control. Has ANNOVAR pipeline.
* Note: if you export table in vcf format, variants with more than 2 alleles will not be exported
* http://varianttools.sourceforge.net/
* Alternatively, use PLINKSEQ : https://atgu.mgh.harvard.edu/plinkseq/

3. Whenever possible, the first thing you should do is to check variants on known genes of your disease-of-interest.
* http://www.nature.com/nature/journal/v508/n7497/full/nature13127.html

4. If you find a variant-of-interest, visually inspect the alignment using IGV
* https://www.broadinstitute.org/igv/
* Instead of loading the whole BAM file (whole genome) into IGV, you may want to extract your region of interest using samtools  
http://samtools.sourceforge.net/

## If you want to start with fastq files: 

1. GATK Best Practices for DNAseq  
https://www.broadinstitute.org/gatk/guide/best-practices?bpm=DNAseq

2. BWA for alignment of reads

3. Picard for mark duplicates  
http://broadinstitute.github.io/picard/

## If you would like to understand the NGS pipeline that GCF used 
https://bcbio-nextgen.readthedocs.org/en/latest/

## Others
* Bedtools  
Interval (BED file) manipuation and check read coverage  
http://bedtools.readthedocs.org/en/latest/content/bedtools-suite.html





