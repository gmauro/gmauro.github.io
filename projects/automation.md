---
layout: subpage
title: Messages-driven automation system for large-scale sequencing center (a.k.a. PRESTA)
---

PRESTA is a Python application that handles sequencing data produced from a large scale NGS Core facility. It leverages a reliable distributed task queue to create a messages-driven automation system. Presta is focused on real-time operation, but supports batch scheduling as well.

Managing tasks and messages, PRESTA is so able to automatically orchestrate format conversion, demultiplexing, quality checks, LIMS update and data preparation for on-site storage or delivery to external sites.

PRESTA is currently part of the [CRS4 fully automated infrastructure](http://next.crs4.it) to support bioinformatics analysis of sequencing data.

PRESTA proudly relies on [Ansible](https://www.ansible.com), [Celery](http://www.celeryproject.org/), [Docker](https://www.docker.com), [RabbitMQ](http://www.rabbitmq.com/)

#### Tasks currently supported:

* Monitoring of the state of an Illumina rundir
* Illumina bcl2fastq software execution at the end of the sequencer's run
* Production of a detailed quality report on sequencing data coming from the previous step
* Updating the activities details on the LIMS portal
* Data delivery to a remote FTP folder, to an iRODS collection, to a local/remote filesystem path or to a removable device.
* Querying the LIMS portal to retrieve details about the data produced

#### Git repositories

* [PRESTA](https://github.com/gmauro/presta)
* [RabbitMQ multi-container](https://github.com/gmauro/rabbitmq-multi-container)
* [Flower docker](https://github.com/gmauro/flower-docker)
* [Delivery service](https://github.com/gmauro/delivery_service)

#### Docker images

* [https://hub.docker.com/r/gmauro/flower](https://hub.docker.com/r/gmauro/flower)

![Presta_architecture](../presta.png)

### Further Reading

1. Cuccuru, G. et al. (2014). An Automated Infrastructure to Support High-troughput Bioinformatics. In Proceedings of. IEEE International Conference on High Performance Computing & Simulation , 07/2014, pages 600-607.  
DOI: 10.1109/HPCSim.2014.6903742.
