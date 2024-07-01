1) git clone
2) terraform apply
3) updates the local kubectl with AWS credentials:
	aws eks --region us-west-1 update-kubeconfig --name terraform-eks-demo
4) Get an OIDC provider for eksctl:
	eksctl utils associate-iam-oidc-provider --region=us-west-1 --cluster=terraform-eks-demo --approve
5) Remove the aws-load-balancer-controller service account appears from terraform
6) Re-create the service account in "EKS Troubleshooting"
7) Create the CRD
8) Install the aws-load-balancer-controller
9) Create the game-2048 namespace
10) Create the webhook service
11) Install the Deployment, Service and Ingress for the game-248
12) Get the FQDN from the kubectl get ingress -n game-2048
