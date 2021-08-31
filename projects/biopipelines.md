---
layout: subpage
title: Next-gen Bioinformatics workflows
---

Next Generation Sequencing projects are rapidly increasing in a huge numbers of laboratories worldwide and with them the needs to ensure **reproducibility** and **portability** of the analysis workflows.  
This requires a transition from the classical “spaghetti code” approach to a more reliable and efficient solutions provided by the modern analysis workflow management systems.  
[Snakemake](https://snakemake.readthedocs.io) is one of the most adopted workflow management system that provides all the features needed to create reproducible and scalable data analyses ensuring a logic separation between the workflow description and its execution details.
Snakemake can handle software dependencies using Conda or Docker and can execute workflows on a great number of different computing environments such as workstations, HPC clusters and clouds. All this features need an environment properly configured for each different setup (e.g. HPC, cloud,...).  
To facilitate the reproducibility and portability of NGS pipelines, we have develop SOLIDA, a Python command-line tool that can easily organize the deployment, the data management and the execution of a Snakemake based workflow.

### Methods
SOLIDA is command-line solution that can easily bootstrap any Snakemake workflow organizing its activity in different properly configured projects. Each project can be different for pipeline code, input data, workflow configuration, virtual environment and/or working folder.  
SOLIDA downloads each pipeline (e.g. exome, RNA-Seq, smallRNA-Seq) from a git repository into a cache store, records its version number and provides an installation profile that can be easily customized by the user to match his settings.  
SOLIDA then deploys for each project, the pipeline to the target computing environment through an Ansible playbook, as follows:
* creation of a dedicated Conda virtual environment
* installation into the Conda virtual environment of all the dependencies needed by the pipeline
* creation of a time labeled working directory containing the pipeline code together with a convenient bash script for its execution

![Solida](../solida.png)

A set of different “ready to go” pipelines have been included in solida:

* Germline and somatic short variant discovery (SNPs + Indels)
* Germline copy number variant discovery (CNVs)
* Variant annotation
* Differential expression analysis (RNA and smallRNA)
* Gene fusion discovery

but other can be added quickly.

![Dima](../dima_dag.png)

SOLIDA is routinely used for complex large-scale genetic analysis by [CRS4 Next generation Sequencing Core Facility](http://next.crs4.it) in a broad range of applications:
* whole-genome
* transcriptome and non coding RNA Sequencing
* human exome
* targeted resequencing

SOLIDA is available through the Python Package Index (PyPI) repository at 
[https://pypi.org/project/solida/](https://pypi.org/project/solida/)



#### Git repositories

* [Solida](https://github.com/solida-core/solida)
* [Biopipelines](https://github.com/solida-core/)


