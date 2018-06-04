# Kops Helper

## Local Requirements

Get latest versions of all below:

- kops
- kubectl
- aws
- jq
- gettext
- helm

If running on macOS and using homebrew, to run gettext and specifically envsubst, you may need to run the following:
<<<<<<< HEAD
```
brew install gettext
brew link --force gettext
```
=======
brew install gettext
brew link --force gettext
>>>>>>> 8f33d04e33de231df9b603a24c0d4124b017d243

## AWS

- Create your AWS Account
- Setup AWS API Keys with permissions to write to IAM, S3, EC2, Route53

## Setting up your cluster

1. Clone this repo
2. Create a file, `kube-setup/setup-vars`, following the template:
```
export AWS_ACCESS_KEY_ID=''
export AWS_SECRET_ACCESS_KEY=''
export SSH_PUBLIC_KEY_FILE=''
export AWS_REGION='us-east-1'
export ROOT_DOMAIN='example.com'
export DOMAIN="kube.$ROOT_DOMAIN"

export NODE_COUNT=3
export AUTO_SCALER_MIN=$NODE_COUNT
export AUTO_SCALER_MAX=10
export NODE_VOLUME_SIZE=100
export NODE_SIZE='m4.large'
export MASTER_SIZE='t2.medium'

export DATADOG_API_KEY=''

export USE_BASTION="true" # true or false
```

3. Run ./kube-setup/setup-cluster
4. Run through the prompts to setup your cluster.

## Resources

Kubernetes
1. Website: http://kubernetes.io/
2. Cluster Auto Scaling: https://github.com/kubernetes/autoscaler/tree/master/cluster-autoscaler/cloudprovider/aws
3. Heapster: https://github.com/kubernetes/heapster
4. Children’s Guide: https://deis.com/blog/2016/kubernetes-illustrated-guide/ (a little outdated but worth a read)

AWS CLI
1. Download: https://aws.amazon.com/cli/  

Kops
1. GitHub: https://github.com/kubernetes/kops 
2. Getting started: https://github.com/kubernetes/kops/blob/master/docs/aws.md
3. Bastion: https://github.com/kubernetes/kops/blob/master/docs/bastion.md 

Helm
1. Website: https://helm.sh 
2. Apps to install: https://hub.kubeapps.com
3. GitHub: https://github.com/kubernetes/helm

Grafana
1. Website: https://grafana.com

## Contributors

- Darye Henry
- Preston Sego

