# deploy-dask-cluster-on-aws

This repo shows how to setup a dask cluster with EC2 instances. The steps under part 1 and 2 have been repeated a couple of times and it worked well.

## Part 1

This is the basic part covered in `start and prepare ec2 instances` (needs to be rename). This show step by step how to setup up all resources using the AWS management console.

#### ToDo
- improve the whole setup such that we can exactly replicate the local environment and the environment on the EC2 instance (e.g. lock dependencies or use containers)

## Part 2

Since the manual steps take time and are error prone a CloudFormation template is provided that creates all resources automatically. This way you have the dask cluster running in about 10 minutes. 

#### ToDo
- Now the number of workers is hard coded. Make this a parameter and use autoscaling to set the number of workers.
- also make the instance type a parameter.

## reference

For now this will be relatively empty repo with just a reference to a good blog

https://saturncloud.io/blog/how-to-set-up-a-dask-cluster/

The blog was not fully working but with a few adjustments I was able to get it running:

- The blog was not really clear on setting the port
- next opening the port on 8787 and 8786 for in bound traffic from the security group we also need to open 8787 to our the world or our IP adress to see the dashboard.
- The range of for the worker ports was too small. Also port in the 30000-40000 range are needed.
- using an Ubuntu OS I needed to create a virtual env.

## ToDo
- as an extra exercise we could try to create a dask cluster using docker.
