# Deeploc2.0

*The deeploc2_final.sif file is located in the shared folder in the roth lab directory.

# Usage

```
-flags

  -f, --fasta. Input in fasta format of the proteins.
  -o, --output. Output folder name.
  -m, --model. High-quality (Accurate) model or high-throughput (Fast) model. Default: Fast.
  -p, --plot. Plot and save attention values for each individual protein. 
```

Using the .sif file is reliant on the container platform singularity. To see if singularity is available in the cluster, enter the following in the command line: 

```
module avail
```

If singularity is an option, enable access by entering:
```
module lode singularity
```

<br>

**Interactive Mode**

Run the srun command with additional flags such as the following:
```
srun --pty -p dept_cpu /bin/bash
```
Then enter the following line into the command prompt:
```
singularity exec "/net/dali/home/roth/shared/deeploc2.0/deeploc2_final.sif" deeploc2 -f input.fasta -o output_directory
```

<br>

**Batch Mode**

-include the line in the script file
```
singularity exec --bind $PWD "/net/dali/home/roth/shared/deeploc2.0/deeploc2_final.sif" deeploc2 -f your_file.csv -o output_dir
```
Then submit the script to SLURM using sbatch:
```
sbatch script.sh
```
