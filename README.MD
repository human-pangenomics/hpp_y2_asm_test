## Year 2 Assembly Testing

![White Logo](https://s3-us-west-2.amazonaws.com/human-pangenomics/backup/logo-proof-full.png)

This repo contains produced by the [Human Pangenome Reference Consortium](https://humanpangenome.org/) from year 2 data. Two assembly methods are tested:
* Verkko
* Hifiasm (w/ ONT UL integration) 

Assemblies for 10 year 2 samples plus HG002 are available. These assemblies are made available for internal HPRC quality control. For information about data reuse and publicating with HPRC data please see the HPRC's [Data Use Protocol](https://humanpangenome.org/data-use-protocol/).

------------------

### Obtaining assemblies

Assemblies are available on our [S3 bucket](https://s3-us-west-2.amazonaws.com/human-pangenomics/index.html?prefix=submissions/53FEE631-4264-4627-8FB6-09D7364F4D3B--ASM-COMP/). The easiest way to download them is to use the URIs provided in the assembly_indexes folder of this repository. Once you have the URIs you can download the assemblies for free using the AWS CLI. For example:
```
aws s3 --no-sign-request cp \
	s3://human-pangenomics/submissions/53FEE631-4264-4627-8FB6-09D7364F4D3B--ASM-COMP/HG002/assemblies/verkko/HG002.verkko_filt_mat.contigs.fa.gz \
	./

```

### Assembly File Types

Raw assembly outputs as well as filtered assemblies are available for download.
* hifiasm_0.18.2_raw.txt\tHifiasm assemblies (raw)
* hifiasm_0.18.2_filtered.txt\tHifiasm assemblies after filtering out contigs >100kb
* verkko_v1.2_raw.txt\tVerkko assemblies (raw)
* verkko_v1.2_filtered.txt\tVerkko assemblies after filtering out contigs/scaffolds >100kb
* verkko_v1.2_filtered_contigs.txt\tVerkko assemblies after filtering out contigs/scaffolds >100kb, then breaking on N's

If you aren't sure which assemblies to use, you probably want the filtered (and unbroken) assemblies.