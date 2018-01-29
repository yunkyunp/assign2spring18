# assign2spring18

# This is an H1 large tag ## This is an H2 large header tag ###### This is an <h6> tag
*This text will be italic* _This will also be italic_  **This text will be bold** __This will also be bold__ 

hostname;
cd~    ls -R;
last | head -5
wget ftp://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/release/NA12878_HG001/NISTv3.3.2/GRCh37/HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf.gz
wget https://samtools.github.io/hts-specs/VCFv4.2.pdf
ls -lh
wc -l < NA12878.variants.vcf
grep -v "#" HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | cut -d "        " -f1 | sort | uniq;                                                                       grep -v "#" HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | cut -d "        " -f 10 | cut -d ":" -f 1 | sort | uniq
grep "0|1:" HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | cut -d "        " -f 10 | cut -d ":" -f 1 | sort | uniq | wc -l
chmod 755 command.py
echo ";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r "gene_symbol=(.*?);"
echo ";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r "gene_sequence=(.*?);"
printf (";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r “gene_symbol=(.*?);”);
printf -v x $(printf ";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r "gene_sequence=(.*?);"); printf -v z $(printf ";gene_symbol=PTEN;gene_name=phospho;gene_sequence=atc;" | pymatch.py -r "gene_name=(.*?);"); echo $z,$x
