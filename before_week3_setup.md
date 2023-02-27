# Build the conda environment 

We'll explain more details on building a conda environment in the workshop. For now, follow instructions below to build the environment. 

## Set up conda channels 

Run the following commands line by line: 

```sh
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

## Create the conda environment

```sh
conda create --name intro-to-linux 
```

Type "y" and press ```enter``` to proceed. 

## Activate the conda environment 

```sh
conda activate intro-to-linux
```

Make sure you have the environment name at the beginning of your command line, then proceed to the install software part. 

![conda_env](./images/conda_environment.png?raw=true) 

## Install the needed software 

Run the following commands line by line:

```sh
conda install -c bioconda fastqc
conda install -c bioconda trimmomatic
conda install -c bioconda bwa
conda install -c bioconda samtools
conda install -c bioconda bcftools 
```

# Copy the data files to your own directory 

Run the following commands line by line: 

```sh
mkdir -p ~/intro_to_linux/data/untrimmed_fastq
cd ~/intro_to_linux/data/untrimmed_fastq
cp /home/u1133824/intro_to_linux/data/untrimmed_fastq/*.gz . 
```