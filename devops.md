---
layout: page
title: DevOps
---
<p class="message">
   "Better collaboration, tighter integration, automation, easy deployments and much less headaches. Trust me ;-)" 
</p>
 What is DevOps? See an [introduction](https://www.atlassian.com/devops) to the argument.
 
   [Ansible](https://www.ansible.com) is a radically simple IT automation platform that automates cloud provisioning, configuration management, application deployment and many other IT needs.
   
 Here a collection of my Ansible projects or I have contributed to:

## [Elasticluster](https://github.com/gc3-uzh-ch/elasticluster)
ElastiCluster aims to provide a user-friendly command line tool to create, manage and setup computing clusters hosted on cloud infrastructures (like Amazon's Elastic Compute Cloud EC2, Google Compute Engine, or a private OpenStack cloud). Its main goal is to get your own private cluster up and running with just a few commands.

## [Galaxy4Training](https://github.com/gmauro/galaxy4training)
Build in a snap a Galaxy environment for a training classroom of 20-30 participants to allow high interactivity and shared practical work.

## [SOLIDA](https://github.com/gmauro/solida)
SOLIDA is command-line solution that facilitate the reproducibility and portability of NGS pipelines. It can easily organize the deployment, the data management and the execution of a Snakemake based workflow.

## [Boxed iRODS](https://github.com/gmauro/boxed-irods)
iCAT server, installed from iRODS binaries, and postgresql server executed from the same host; everything enabled by Ansible.  
This repository contains also Dockerfile for iRODS automated build published to the Docker Hub Registry.  
Useful for testing/development.

## [Delivery service](https://github.com/gmauro/delivery_service)
This repo contains an Ansible role to deploy a delivery service consinsting of a WebDAV server (Apache2 enabled) and an FTPES server (Proftpd enabled).  
Both servers use the same data path and users can retrieve data indifferently from the WebDAV or FTPES server.  
All the communications are encrypted using SSL enabled data channel.

# Ansible roles
Roles are ways of automatically loading predefined tasks into an Ansible playbook.

As example, [Dotfiles](https://github.com/gmauro/dotfiles) is my Ansible playbook to configure my own workstation (base system and app dotfiles/configurations). It make use of several Ansible roles listed here.

## [Ansible Bika.webservice](https://github.com/gmauro/ansible-bika.webservice)
Ansible role to install [bika.webservice](http://github.com/ratzeni/bika.webservice) on Ubuntu or Debian systems.

## [Ansible Docker](https://github.com/gmauro/ansible-docker)
Ansible role to install [Docker-CE](http://www.docker.com) and extensions on Ubuntu or Debian systems . 

## [Ansible Galaxy OS](https://github.com/galaxyproject/ansible-galaxy-os)
Ansible role for configuring the base operating system useful for running [Galaxy](https://github.com/galaxyproject/galaxy).

## [Ansible Galaxy Extras](https://github.com/gmauro/ansible-gx-extras)
Ansible role to configure several production services as nginx, uwsgi and supervisor.

## [Ansible ICE](https://github.com/gmauro/ansible-ice)
Ansible role to install [Ice](https://zeroc.com/products/ice) into a Debian or Ubuntu system.

## [Ansible Java](https://github.com/gmauro/ansible-java)
Ansible role to install Java on Ubuntu or Debian systems.

## [Ansible OMERO.biobank server](https://github.com/gmauro/ansible-obb-server)
An Ansible role to install [OMERO.biobank](https://github.com/crs4/omero.biobank) server into an Ubuntu or Debian system.

## [Ansible PlayOnlinux](https://github.com/gmauro/ansible-playonlinux)
Ansible role to install [PlayOnLinux](http://www.playonlinux.com) on Ubuntu or Debian systems.

## [Ansible Postgresql](https://github.com/gmauro/ansible-postgresql)
Ansible role to install a [PostgreSQL](https://www.postgresql.org) server on Ubuntu or Debian systems
