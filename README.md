# Building Infrastructure Using terraform
terraform init
terraform apply --auto-approve

# update the configuration of EKS
aws eks update-kubeconfig --name EKS_CLOUD --region us-east-1

# Creation of deployment and service for EKS
kubectl apply -f deployment.yaml 

# Create the service
kubectl apply -f service.yaml

# Details of your application
kubectl describe service mario-service

# Destroy all the Insrastructure
kubectl delete service mario-service
kubectl delete deployment mario-deployment
cd EKS-TF
terraform destroy --auto-approve





