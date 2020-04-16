# Kops
- Install kops

### Exports
`
export KOPS_CLUSTER_NAME=avi.k8s.local
export KOPS_STATE_STORE=s3://kops.avi.devops
`

### Cluster Creation
`
- kops create cluster --node-count=1 --node-size=t2.micro --master-size=t2.micro --zones=us-east-1a --name=${KOPS_CLUSTER_NAME} --ssh-public-key=~/.ssh/secret_key.pub
- kops get cluster
- kops edit cluster ${KOPS_CLUSTER_NAME}
- kops update cluster --name ${KOPS_CLUSTER_NAME} --yes
`


# KubeCtl
- Install KubeCtl

### Pod Creation
`
- kubectl create -f sample.yaml
- kubectl apply -f sample.yml
- kubectl edit {PODS/SERVICE} 
`

# EKS
`
- Create VPC and respective details
- Go to AWS EKS console, create an EKS cluster
- aws eks update-kubeconfig --name {cluster-name}

`
