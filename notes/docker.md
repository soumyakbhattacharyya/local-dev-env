# Basic
* core difference between virtualization and containerization

|             virtualization             	|                     containerization                    	|
|:--------------------------------------:	|:-------------------------------------------------------:	|
| based on hardware level virtualization 	| based on operating system level virtualization          	|
| heavyweight                            	| lightweight                                             	|
| slow provisioning                      	| real time provisioning and scalability                  	|
| fully isolated and secure              	| less isolated as only guarantee process level isolation 	|

* lxc 
  * The Linux kernel provides the cgroups functionality that allows limitation and prioritization of resources (CPU, memory, block I/O,
network, etc.) without the need for starting any virtual machines, and namespace isolation functionality that allows complete isolation
of an applications' view of the operating environment, including process trees, networking, user IDs and mounted file systems.

## Installation

* on ubuntu systems
  * approach - 1
  ```sh
   sudo apt-get update 
   sudo apt-get install -y docker.io
   sudo ln -sf /usr/bin/docker.io /usr/local/bin/docker
   ```
  * explanation - default installation of docker, may not get the latest. there preexist a package named "docker" that is docker package is termed as "docker.io". last command creates a soft link to docker.io executable as docker
  * approach - 2
  ``` sh
   # add the new gpg key
   apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
   # edit your /etc/apt/sources.list.d/docker.list
   vim /etc/apt/sources.list.d/docker.list
   # remove the contents and replace with the following depending on your os and version:
   # Ubuntu Trusty 
   deb https://apt.dockerproject.org/repo ubuntu-trusty main
   apt-get update
   #remove the old
   apt-get purge lxc-docker*
   # install the new
   $ apt-get install docker-engine
   ```
   * explanation 
  








