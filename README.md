[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/QRyGulzo)
# Intro to Snakemake Precept

## Overview

This precept will introduce you to the Snakemake workflow management system. You will access the Adroit cluster, clone the repository, and run an example Snakemake pipeline.

Ensure you document the output you use to complete the exercises. Submitting a text file with the changes you make is sufficient.

## Exercise 1: Accessing and Cloning a Repository on Adroit

Follow the guide for [accessing the Adroit cluster](https://researchcomputing.princeton.edu/systems/adroit#access).

- **Objective**: Access the Adroit HPC cluster and clone a repository.
- **Tasks**:
    1. Use SSH to connect to the Adroit cluster.
    2. Authenticate with GitHub! This may be a bit tricky. You may need to generate an SSH key and add it to your GitHub account. See [this guide](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh) for more information.
    3. Clone the repository: `git clone [your assignment repository URL]`.

## Exercise 2: Running a Snakemake Pipeline on Adroit

In this exercise, you will run an example Snakemake pipeline that converts FASTQ files to VCF format. The base and data for this Snakemake workflow can be found at `/scratch/swwolf/snakemake_workflow/fastq_2_VCF` on Adroit.

- **Objective**: Learn to run a Snakemake pipeline.
- **Tasks**:
    1. Load anaconda (`module load anaconda3/2023.9`) and create an environment for snakemake `conda env create -f /scratch/swwolf/snakemake_workflow/fastq_2_VCF/bioinformatics.yml`.
    2. Activate the environment with `conda activate bioinformatics`.
    3. Make a directory for yourself in scratch `mkdir /scratch/$USER`
    4. Copy the directory `/scratch/swwolf/snakemake_workflow/fastq_2_VCF` to your home folder (`cp -r /scratch/swwolf/snakemake_workflow/fastq_2_VCF /scratch/$USER`)
    5. Move the the fastq_2_VCF folder (`cd /scratch/$USER/fastq_2_VCF`
    6. Examine the Snakemake file to understand the workflow steps. You can open the file in vscode, open the file in a terminal based text editor like vim or emacs `vim Snakefile` or `emacs Snakefile` or `nano Snakefile`, or just look at the file contents with `cat Snakefile`
    7. Run the Snakemake pipeline: `snakemake --cores [number_of_cores]`.
    8. Verify the output to ensure the pipeline ran successfully.

## Exercise 3: Modifying the Snakemake Pipeline

After successfully running the example pipeline, make a minor modification to the workflow.

- **Objective**: Gain experience in modifying and understanding the components of a Snakemake pipeline.
- **Tasks**:
    1. Choose a simple modification to make (e.g., changing a parameter in one of the steps, modifying the output format, or adding a simple rule).
    2. Edit the Snakemake file to implement your modification.
    3. Rerun the pipeline to incorporate your changes: `snakemake --cores [number_of_cores]`.
    4. Check the new output to ensure your modification was successful.

Remember to document all changes and any observations you make while completing these exercises.
