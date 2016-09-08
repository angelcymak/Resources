# NGS

## If you already have VCF files:

1. Quality control, a post:  
http://www.cureffi.org/2012/10/17/descriptive-statistics-and-quality-control-on-variants/

    Variant evaluation using GATK
    https://www.broadinstitute.org/gatk/guide/tooldocs/org_broadinstitute_gatk_tools_walkers_varianteval_VariantEval.php  
    https://www.broadinstitute.org/gatk/guide/tagged?tag=varianteval  
    By samples: http://gatkforums.broadinstitute.org/discussion/1994/varianteval-on-multisample-calling-vcf

2. Annotate, manipulate, query variants using Variant tools (vtools)  
Can also perform association. Good tutorial on quality control. Has ANNOVAR pipeline.  
Note: if you export table in vcf format, variants with more than 2 alleles will not be exported  
http://varianttools.sourceforge.net/  

  Alternatively, use PLINKSEQ  
  https://atgu.mgh.harvard.edu/plinkseq/  

3. Whenever possible, the first thing you should do is to check variants on known genes of your disease-of-interest.  
http://www.nature.com/nature/journal/v508/n7497/full/nature13127.html  

  The American College of Medical Genetics and Genomics has published recommendations about reporting incidental findings in the exons of certain genes.  
  http://www.ncbi.nlm.nih.gov/clinvar/docs/acmg/

4. If you find a variant-of-interest, visually inspect the alignment using IGV  
https://www.broadinstitute.org/igv/  

  Instead of loading the whole BAM file (whole genome) into IGV, you may want to extract your region of interest using samtools  
  http://samtools.sourceforge.net/
  
5. Be aware that you may always have a few variants on certain large or highly polymorphic genes, like Titan. See discussions on this topic:  
  https://www.biostars.org/p/51446/


## If you want/need to start with fastq files: 

1. QC your fastq files using FASTQC  
http://www.bioinformatics.babraham.ac.uk/projects/fastqc/ 

2. GATK Best Practices for DNAseq  
https://www.broadinstitute.org/gatk/guide/best-practices?bpm=DNAseq

3. BWA for alignment of reads  
http://bio-bwa.sourceforge.net/

4. Picard for mark duplicates  
http://broadinstitute.github.io/picard/

5. Picard for summary statistics of BAM files  
https://broadinstitute.github.io/picard/command-line-overview.html#CalculateHsMetrics  

## If you would like to understand the NGS pipeline that GCF uses (2015, may be obsolete)  
https://bcbio-nextgen.readthedocs.org/en/latest/

## If you have small targeted regions  
1. May need VariantFiltration (hard filtering) instead of VQSR depending on the size of the targeted region  
http://gatkforums.broadinstitute.org/discussion/3794/failed-in-variantrecalibrator-for-my-customized-target-re-sequencing-data  

2. BQSR may not work if region is <100M bases  
http://gatkforums.broadinstitute.org/discussion/4272/targeted-sequencing-appropriate-to-use-baserecalibrator-bqsr-on-150m-bases-over-small-intervals

## Others
* Bedtools  
Interval (BED file) manipuation and check read coverage  
http://bedtools.readthedocs.org/en/latest/content/bedtools-suite.html

* Phased vcf  
https://www.broadinstitute.org/gatk/guide/article?id=45

* Imputation  
  Michigan Imputation Server (most convenient)  
  https://imputationserver.sph.umich.edu/index.html

  Beagle  
  http://faculty.washington.edu/browning/beagle/beagle.html  

  VCF to Beagle input  
  https://www.broadinstitute.org/gatk/guide/tooldocs/org_broadinstitute_gatk_tools_walkers_beagle_ProduceBeagleInput.php  
  
* Convert file format: plink to vcf  
  http://www.researchgate.net/post/How_to_convert_plink_files_to_VCF_or_other_easily_parseable_format2


## Tools I heard but haven't tried  
* vcf manipulation  
  http://snpeff.sourceforge.net/SnpSift.html#TsTv


## Reading
* Recommended depth of coverage    
https://genohub.com/recommended-sequencing-coverage-by-application

* Guidelines for investigating causality of sequence variants in human disease
MacArthur et al., Nature, 2014 Apr
http://www.nature.com/nature/journal/v508/n7497/full/nature13127.html

* Exome sequencing as a tool for Mendelian disease gene discovery
Bamshad et al., Nature Rev. Genet. 12, 745–755 (2011)
http://www.nature.com/nrg/journal/v12/n11/full/nrg3031.html

* Exome sequencing and the genetic basis of complex traits
Kiezun et al., Nature Genet. 44, 623–630 (2012)
http://www.nature.com/ng/journal/v44/n6/full/ng.2303.html



## Contributors  
Sulggi Lee


