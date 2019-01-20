---
layout: subpage
title: Laboratory Information Management System
---

At CRS4 NGS core facility, all activities on the wet-lab side are tracked using [BIKA-LIMS](https://www.bikalims.org/), an open source, community based LIMS.

BIKA-LIMS handles roles and authorisations,  manages the inventory and the supply chain,  tracks samples, prioritizes analysis requests and easily organize worksheets per project.

This project has created a specialized  web interface, based on an AngularJS and a REST web-service, to expose LIMS data to the wet-lab technicians.

The components are deployed by [Ansible](https://www.ansible.com) and executed as a [multi-container Docker](https://docs.docker.com/compose/) application.

#### Git repositories

* [AroundBika](https://github.com/crs4/aroundBika)
* [Ansible Bika.webservice](https://github.com/gmauro/ansible-bika.webservice)
* [Bika.penelope](https://github.com/ratzeni/bika.penelope)
* [Bika.webservice](https://github.com/ratzeni/bika.webservice)
* [Bika.client](https://github.com/ratzeni/bika.client)

![AroundBika](../lims.png)


    
