**************************************************************************************************************
# SIMULATING AND ASSEMBLING READS FROM A LOCUSTA MIGRATORY CONTIG
**************************************************************************************************************
This project simulates reads from the Locusta Migratory genome assembly using wgsim and assembles the reads using SOAPdenovo. Various parameters are tested to see their affect on the assembly. This project is meant to run on IU's Carbonate HPC, for which you can simply clone this repository and execute the run_assembly.txt file while inside the 'genomeassembly' directory to reproduce all results.

run_assembly.txt loads the singularity module, downloads an already built singularity image from sylabs, and runs all of the commands located in biovino_record.txt from the singularity container which contains all of the necessary packages to reproduce the results found in this project.

biovino_record.txt downloads the Locusta migratoria genome assembly from https://www.ncbi.nlm.nih.gov/data-hub/genome/GCA_000516895.1/ which is a list of all assembeled contigs from this particular genome in fasta format. The seqkit package is used to parse through the contigs to find the 7th largest contig. From there, random reads are generated using wgsim and reassembled using SOAPdenovo2. Five different read simulations and assemblies are performed to understand how the various parameters affect contig/scaffold assembly.

biovino_se.config and biovino_se.config are parameter files necessary for SOAPdenovo2.

biovino_sing.def was used to build the singularity image file for this project, but it is not required to use it in any way to recplicate the results. The image is stored on sylabs and is pulled remotely in order to simplify the process of replicating this work.
