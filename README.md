# bbdocker
Docker image for latest BioBuilds

This Debian-based Docker image installs dependencies for conda, miniconda, and then installs the latest release of BioBuilds. See the [BioBuilds website](http://www.biobuilds.org/) for more details on the bioinformatics-related packages available.

## Quickstart
Download the Dockerfile and build the image:
```bash
wget --no-check-certificate https://raw.githubusercontent.com/keithcallenberg/bbdocker/master/Dockerfile
docker build -t bbdocker ./
```

Run the built image (bash is entrypoint):
```bash
docker run -ti bbdocker
```

All BioBuilds-provided tools are now on your path:
```
root@8ca18cc97a30:/# samtools

Program: samtools (Tools for alignments in the SAM format)
Version: 1.3 (using htslib 1.3)

Usage:   samtools <command> [options]

Commands:
  -- Indexing
     dict           create a sequence dictionary file
     faidx          index/extract FASTA
     index          index alignment
  ...

```

