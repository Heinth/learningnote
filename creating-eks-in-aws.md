# Creating EKS in AWS

```
# eksctl create cluster --name aws-eks-demo --version 1.22 --region ap-southeast-1 --nodegroup-name eks-demo-workers --node-type t2.micro --nodes 3 --nodes-min 1 --nodes-max 4 --managed
# aws eks update-kubeconfig --name aws-eks-demo --region ap-southeast-1 
# kubectl get nodes
```
