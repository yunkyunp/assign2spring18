## 1
hostname
## 2
cd~    ls -R
## 3
last | head -5
## 4
wget ftp://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/release/NA12878_HG001/NISTv3.3.2/GRCh37/HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf.gz
## 5
wget https://samtools.github.io/hts-specs/VCFv4.2.pdf
## 6a
ls -lh
## 7
wc -l < NA12878.variants.vcf
## 8a
grep -v "#" HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | cut -d "        " -f1 | sort | uniq;                                                                       grep -v "#" HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | cut -d "        " -f 10 | cut -d ":" -f 1 | sort | uniq
## 8b
grep "0|1:" HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | cut -d "        " -f 10 | cut -d ":" -f 1 | sort | uniq | wc -l
## 9
chmod 755 command.py
## 10
printf -v x $(printf ";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r "gene_sequence=(.*?);"); printf -v z $(printf ";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r "gene_name=(.*?);"); echo $z,$x
