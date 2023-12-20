# EggNOG-mapper v2.1.12 container

## Informations

Main tool: [eggNOG-mapper](http://eggnog5.embl.de/#/app/home) \
Version: 2.1.12

Description: **EggNOG-mapper is a tool for fast functional annotation of novel sequences.**

GitHub: [https://github.com/eggnogdb/eggnog-mapper](https://github.com/eggnogdb/eggnog-mapper) 

## Citations

1. eggNOG-mapper v2: functional annotation, orthology assignments, and domain prediction at the metagenomic scale. Carlos P. Cantalapiedra, Ana Hernandez-Plaza, Ivica Letunic, Peer Bork, Jaime Huerta-Cepas. 2021. Molecular Biology and Evolution, msab293, https://doi.org/10.1093/molbev/msab293
2. eggNOG 5.0: a hierarchical, functionally and phylogenetically annotated orthology resource based on 5090 organisms and 2502 viruses. Jaime Huerta-Cepas, Damian Szklarczyk, Davide Heller, Ana Hernández-Plaza, Sofia K Forslund, Helen Cook, Daniel R Mende, Ivica Letunic, Thomas Rattei, Lars J Jensen, Christian von Mering, Peer Bork Nucleic Acids Res. 2019 Jan 8; 47(Database issue): D309–D314. doi: 10.1093/nar/gky1085 

Cite also the underlying algorithm used for the search step of eggNOG-mapper, and Prodigal if it was used for gene prediction:

* **HMMER**: Accelerated Profile HMM Searches. Eddy SR. 2011. PLoS Comput. Biol. 7:e1002195.
* **DIAMOND**: Sensitive protein alignments at tree-of-life scale using DIAMOND. Buchfink B, Reuter K, Drost HG. 2021. Nature Methods 18, 366–368 (2021). https://doi.org/10.1038/s41592-021-01101-x
* **MMSEQS2**: MMseqs2 enables sensitive protein sequence searching for the analysis of massive data sets. Steinegger M & Söding J. 2017. Nat. Biotech. 35, 1026–1028. https://doi.org/10.1038/nbt.3988
* **PRODIGAL**: Prodigal: prokaryotic gene recognition and translation initiation site identification. Hyatt et al. 2010. BMC Bioinformatics 11, 119. https://doi.org/10.1186/1471-2105-11-119.

## License

[The original egNOG-mapper license still applies to this container](https://github.com/eggnogdb/eggnog-mapper/blob/master/LICENSE.txt)

## Build egNOG-mapper Singularity image

```bash
singularity build eggnog-mapper_2.1.12.sif eggnog-mapper_2.1.12.def
```

## Using eggNOG-mapper

### Download database

The database used by eggnog is integrated into the container. [WARNING](https://github.com/eggnogdb/eggnog-mapper/wiki/eggNOG-mapper-v2.1.5-to-v2.1.12#user-content-Setup) use of -y option: assume "yes" to all questions
```bash
python download_eggnog_data.py
````
The database will be downloaded to the */data* folder

### General use

**Run the application**
```bash
singularity run eggnog-mapper_2.1.12.sif emapper.py <options>
```
* *\<options_\>* : indicate the different options to use

### Example of use

* To get help
```bash
singularity run eggnog-mapper_2.1.12.sif emapper.py --help
```
* Example of use: 

### Interactive shell

To run an interactive shell
```bash
singularity shell eggnog-mapper_2.1.12.sif
```
After this command you work in the container. You can directly execute the different eggNOG-mapper commands.
