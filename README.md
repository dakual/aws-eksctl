Installing eksctl
```sh
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

sudo mv /tmp/eksctl /usr/local/bin

eksctl version

eksctl create cluster --name my-cluster --region region-code
eksctl delete cluster --name my-cluster --region region-code

eksctl create cluster -f cluster.yml
eksctl delete cluster -f cluster.yml

aws eks update-kubeconfig --region eu-central-1 --name demo-eks-cluster
```