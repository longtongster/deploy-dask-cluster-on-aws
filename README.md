# deploy-dask-cluster-on-aws

This repo shows how to setup a dask cluster with EC2 instances. 

- step 1: start and install ec2 instances.

## reference

For now this will be relatively empty repo with just a reference to a good blog

https://saturncloud.io/blog/how-to-set-up-a-dask-cluster/

The blog was not fully working but with a few adjustments I was able to get it running:

- The blog was not really clear on setting the port
- next opening the port on 8787 and 8786 for in bound traffic from the security group we also need to open 8787 to our the world or our IP adress to see the dashboard
- using an Ubuntu OS I needed to create a virtual env.

## ToDo
- write step by step explenation
- create a start up script for the instances
- use poetry for dependency managenent
- as an extra exercise we could try to create a dask cluster using docker.

## Setting up the Cluster

userdata
