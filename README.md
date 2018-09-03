#  Generate sbatch files

Scripts to generate many sbatch for job submitting on Slurm cluster and pipelinining.

The content of `script.sbatch` looks like this:
```
#!/bin/bash
#SBATCH -A project-name
#SBATCH -p core
#SBATCH -n 1
#SBATCH -t 1-00:00:00
#SBATCH -J job-name
#SBATCH -o output.out
#SBATCH -e errors.err

command-to-execute
```

[sbatch.py](sbatch.py) is a custom module that contains all necessary functions. It is loaded as `import sbatch `.

[reads-to-VCF_dog.py](reads-to-VCF_dog.py) - the genomic variant calling pipeline. It is described in this [blog-post](http://evodify.com/genomic-variant-calling-pipeline/)
