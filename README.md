# Deeploc2.0

# Usage

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
singularity exec --bind $PWD deeploc2.sif deeploc2 -f your_file.csv -o output_dir
```
```
sbatch script.sh
```
