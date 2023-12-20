# CD-HIT v4.8.1 container

## Informations

Main tool: [CD-HIT](https://sites.google.com/view/cd-hit) \
Version: 4.8.1

Description: **Cd-hit: a fast program for clustering and comparing large sets of protein or nucleotide sequences**

GitHub: [https://github.com/weizhongli/cdhit](https://github.com/weizhongli/cdhit) 

## Citations

1. Weizhong Li & Adam Godzik. Cd-hit: a fast program for clustering and comparing large sets of protein or nucleotide sequences. Bioinformatics (2006) 22:1658-1659 
2. Limin Fu, Beifang Niu, Zhengwei Zhu, Sitao Wu and Weizhong Li, CD-HIT: accelerated for clustering the next generation sequencing data. Bioinformatics, (2012), 28 (23): 3150-3152. doi: 10.1093/bioinformatics/bts565

## License

[The original CD-HIT license still applies to this container](https://github.com/weizhongli/cdhit/blob/master/license.txt)

## Build CD-HIT Singularity image 

```bash
singularity build cd-hit_4.8.1.sif cd-hit_4.8.1.def
```

## Using CD-HIT

### General use

**Run the application**
```bash
singularity run cd-hit_4.8.1.sif <cd-hit-command-name> <options>
```
* *\<cd-hit-command-name\>* : specify the cd-hit command to use (example: cd-hit, cd-hit-est, cd-hit-454, ...) 
* *\<options_\>* : indicate the different options to use

### Example of use

* For help with the different *CD-HIT* options
```bash
docker run cd-hit_4.8.1.sif cd-hit
```
* Example of use: clustering with 90% identity
```bash
singularity run cd-hit_4.8.1.sif cd-hit -i input.fa -o output -c 0.9 -n 5 -d 0
```

### Interactive shell

To run an interactive shell
```bash
docker shell cd-hit_4.8.1.sif
```
After this command you work in the container. You can directly execute the different CD-HIT commands.
