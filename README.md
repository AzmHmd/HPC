# HPC

ssh user@sunbird.swansea.ac.uk

** what to write in the slurm file:

#!/bin/bash --login
#$ -cwd
#SBATCH --job-name=flip_detection_on_GPU
#SBATCH --out=flip_detection_on_GPU.out.%J
#SBATCH --err=flip_detection_on_GPU.err.%J
#SBATCH -p gpu
#SBATCH --mem-per-cpu=30G
#SBATCH -n 1
#SBATCH --gres=gpu:1

module purge 
module load tensorflow
python test_on_gpu_save_files.py


------------------------------------------------------------------------------------------------

** how to run the code:

sbatch file.slurm

squeue -u a.azh2

---------------------------------------------------------------------------------------------------
