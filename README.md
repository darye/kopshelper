# Kops Helper

## Local Requirements

- kops
- kubectl
- aws
- jq
- gettext

## Seting up your cluster

1. Clone this repo
2. Create a file, `kube-setup/setup-vars`, following the template:
```
export AWS_ACCESS_KEY_ID=''
export AWS_SECRET_ACCESS_KEY=''
export SSH_PUBLIC_KEY_FILE=''
export AWS_DEFAULT_REGION='us-east-1'
export ROOT_DOMAIN='example.com'
export DOMAIN="kube.$ROOT_DOMAIN"

export NODE_COUNT=3
export AUTO_SCALER_MIN=$NODE_COUNT
export AUTO_SCALER_MAX=10
export NODE_VOLUME_SIZE=100
export NODE_SIZE='m4.large'
export MASTER_SIZE='t2.medium'

export USE_BASTION="true" # true or false
```

3. Run ./kube-setup/setup-cluster
4. Run through the prompts to setup your cluster.

## Contributors

- Darye Henry
- Preston Sego

