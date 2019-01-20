---
layout: subpage
title: OMERO.biobank
---

OMERO.biobank is a robust, extensible and scalable traceability framework developed to support large scale experiments in data intensive biology. The data management system is built upon the core services of OME Remote Objects [OMERO](https://www.openmicroscopy.org/index.html), an open source software platform that includes a number of storage mechanisms, remoting middleware, an API, and client applications developed by the Open Microscopy Environment.  
We developed an indexing system implemented by using Neo4j and coupled it to OMERO in order mantain a persistent version of the traceability graph by mapping objects as nodes and actions as edges.  
The data persistence layer and the graph index are kept in sync through an event-oriented architecture based on RabbitMQ: all save, delete or update transactions are mapped as messages, sent to the events engine and consumed by a daemon that directly acts on the graph database. During the query process, users interact with the index engine transparently: queries are redirected to the graph database which responds with a list of nodes and edges descriptions that are used to retrieve real data from OMERO’s database.

#### Demo
A video showing OMERO.biobank coupled with Galaxy executing an automated reanalysis of microbial samples  
[OMERO.biobank demo](https://youtu.be/oXWQcIXR2PA)

#### Git repositories

* [OMERO.biobank](https://github.com/crs4/omero.biobank)


#### Links
* [Development Team at OME](https://www-legacy.openmicroscopy.org/site/about/development-teams/gianluigi)


    
### Further Reading


1. Cuccuru, G. et al. (2014). An Automated Infrastructure to Support High-troughput Bioinformatics. In Proceedings of. IEEE International Conference on High Performance Computing & Simulation , 07/2014, pages 600-607.  
DOI: 10.1109/HPCSim.2014.6903742.

2. C. Allan et al., “OMERO: flexible, model-driven data management for experimental biology,” Nature Methods, vol. 9, no. 3, pp. 245–253, Mar 2012.  
DOI: 10.1038/nmeth.1896
