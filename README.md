# eks_wordpress
These program files can be used to launch a cluster on top of AWS Cloud using EKS service
The cluster would help in launching a WordPress website using MySQL as the back-end database
AWS EFS service is used to provide storage for pods

The following program files need to be updated accordingly:
1. cluster.yaml, at lines 5 to 13
2. create-efs-provisioner.yaml, at lines 20-26
3. create-rbac.yaml, at line 9
4. create-storage.yaml, at line 5

values for some key-value pairs have been commented using "#"
use appropriate values before using them provided and/or used w.r.t. AWS Cloud
a few pre-requisites before using the same:
1. keep a AWS key ready to be used to login to nodes
2. kubectl and eksctl programs on local host are must

To create a cluster for other general purpose use cluster.yaml file
command: eksctl create cluster -f cluster.yaml
Remember to configure kubectl program to use the same cluster
command: aws eks update-kubeconfig --name ekscluster

For a brief and step-by-step description to do the task visit:
https://www.linkedin.com/pulse/aws-eks-service-sarthak-sharma

P.S. the EKS service is not free
So for testing purposes, be sure to delete the cluster after use
command: eksctl delete cluster --name <cluster_name>
