# Deeploc2.0

# Usage

*The deeploc2_final.sif file is located in the shared folder in the roth lab directory.

```
module avail
```
```
module lode singularity
```

Interactive Mode:

-use srun first
```
singularity exec "/net/dali/home/roth/shared/deeploc2.0/deeploc2_final.sif" deeploc2 -f input.fasta -o output_directory
```


Batch Mode:

-include the line in the script file
```
singularity exec --bind $PWD "/net/dali/home/roth/shared/deeploc2.0/deeploc2_final.sif" deeploc2 -f your_file.csv -o output_dir
```
```
sbatch script.sh
```
