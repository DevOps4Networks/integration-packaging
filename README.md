Welcome to the OpenDaylight Integration Packaging project.

This project uses a combination of [Packer](https://www.packer.io), [Vagrant](https://www.vagrantup.com), [Docker](https://www.docker.com) and [Ansible](http://www.ansible.com) to create VMs that can be used for testing, developing, learning and teaching on the [OpenDaylight platform](https://www.opendaylight.org).

#About the Tools Being Used

Before you can use this project to build a VM, you need to install the tools listed below, and, ideally, you should have at least a *passing* knowledge of what they are for. See the "Details" section below for some guidance on what these tools are doing for you, and how.

##Packer

Packer is used to drive the overall VM build process. The Packer installation instructions here [here](https://www.packer.io/intro/getting-started/setup.html).

##Docker

Docker is invoked by Packer to create a Docker image. The Docker installation instructions are [here](https://docs.docker.com/installation/).

Note, on Mac OSX you need to use the "Docker Quickstart Terminal window" to run the build.

##Vagrant

##Virtual Box

#How to Use

Read all the way through this section before attempting any commands.

Clone this project locally, on either a Linux or Mac OS X platform, then (assuming your git directory is in your home directory):

```bash
cd ~/git/integration-packaging/packer/
packer build -var-file=packer_vars.json centos.json
```

Note that these instructions *may* be workable on Windows also, but that has not been tested yet.

On Mac OSX, if you want to build the Docker image, you will need to use the "Docker Quickstart Terminal window" as explained in these [Doscker on OSX instructions](http://docs.docker.com/mac/step_one/). If you try to run the `packer` command above in a "normal" terminal shell, the Docker part of the build will fail.



