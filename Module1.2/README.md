# High-Performance Computing (HPC) Quick Reference Guide

## Basic Guide (Helpful when beginning assignments)
- **Login Node (Head Node):**
  - Upon logging into the cluster, you are on the login node (or head node).
  - You can submit jobs to the queue from the login node but **do not run jobs directly on the login node**. High memory or compute-intensive jobs must be run on compute nodes.

## Transferring Files
Tools for file transfer:
- `scp` (Secure Copy)
- `rsync`
- `sftp` (Secure File Transfer Protocol)
- GUI tools like FileZilla

## SLURM Commands Overview
- `sbatch`: Submit a job.
- `squeue`: Check the status of jobs.
- `sinfo`: Get information about nodes and partitions.
- `scancel`: Delete running or queued jobs.
- `longjob <jobid>`: View details about a specific job.

## Logging Into the Cluster
Use the SSH protocol and one of the following applications:
- `ssh` (command-line tool)
- Putty
- MobaXterm
