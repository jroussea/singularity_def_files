# Diamond v2.1.8 container

## Informations

Main tool: [Diamond](https://github.com/bbuchfink/diamond/wiki) \
Version: 2.1.8

Description: **DIAMOND is a sequence aligner for protein and translated DNA searches, designed for high performance analysis of big sequence data.**

GitHub: [https://github.com/bbuchfink/diamond](https://github.com/bbuchfink/diamond)

## Citations

* Buchfink B, Reuter K, Drost HG, "Sensitive protein alignments at tree-of-life scale using DIAMOND", Nature Methods 18, 366–368 (2021). doi:10.1038/s41592-021-01101-x

For sequence clustering:

* Buchfink B, Ashkenazy H, Reuter K, Kennedy JA, Drost HG, "Sensitive clustering of protein sequences at tree-of-life scale using DIAMOND DeepClust", bioRxiv 2023.01.24.525373; doi: https://doi.org/10.1101/2023.01.24.525373

## License

[The original Diamond license still applies to this container](https://github.com/bbuchfink/diamond/blob/master/LICENSE)

## Build Diamond Singularity image 

```bash
singularity build diamond_2.1.8.sif diamond_2.1.8.def
```

## Using Diamond

### General use

**Run the application**
```bash
singularity run diamond_2.1.8.sif diamond <options>
```
* *\<options_\>* : indicate the different options to use

### Example of use

* To get help
```bash
singularity run diamond_2.1.8.sif diamond
```

### Interactive shell

To run an interactive shell
```bash
singularity shell diamond_2.1.8.sif
```
After this command you work in the container. You can directly execute the different Diamond commands.
