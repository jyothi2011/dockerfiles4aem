# dockerfiles4aem
### Docker environment for AEM

## Abstract
Docker automates the deployment of applications and isolates them inside software containers, by providing an additional layer of abstraction and automation but with out the overhead caused by a virtual machine. 
Here are my dockerfiles for AEM set-up which should be the basis of creating a docker envionment for AEM by just using DOCKER-COMPOSE.


## Required Applications
* [Docker for OSx (native)](https://docs.docker.com/engine/installation/mac/)
* [Docker for Windows (uses HyperV - VMware and VirtualBox will not work anymore)](https://docs.docker.com/engine/installation/windows/)
* [Docker Toolbox (For Windows or OSx using VirtualBox - if VMware and VirtualBox are still a required feature to use on the machine)](https://www.docker.com/products/docker-toolbox)

## Build Prerequisites
The following files are required, but they're not part of this repository. Add them manually before you're able to build the Docker images.
- AEM/aem-quickstart-*.jar (e.g aem-quickstart-6.0.jar)
- AEM/license.properties
- Dispatcher/dispatcher-apache*.*.so (e.g. dispatcher-apache2.4-4.1.8.so)

## Build AEM Images
Execute within the _repository-root_ folder:
```
docker-compose build
```
## Start environment
Execute within the project root folder
```
docker-compose up 
```
or for e.g. only author
```
docker-compose up  author
```
## Access AEM Environment
If you use Docker-Toolbox (or Boot2Docker) you need to identify the "default-VM"'s IP address, to access the AEM on docker:
```boot2docker ip```
or 
```docker-machine ip```

Through this IP you can access the AEM author and publish as well as the Apache dispatcher through the known standard ports.
