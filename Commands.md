# Kubeclt commands

### Set Alias

`
Set-Alias -Name k -value kubectl
`

## Create Pod

`kubectl create -f pod-nginx-server.yml --dry-run --validate=true `
`kubectl create -f pod-nginx-server.yml --save-config --record `
`kubectl run nginx-server --image nginx`


### pod info 
info `kubectl describe pod  `

edit 
- `kubectl edit pod redis`
- `kubectl edit pod <pod-name>`
- `kubectl get pod <pod-name> -o yaml > pod-definition.yaml`

## replication controller - replica set
- `kubectl create -f replicaset-definition`
- `kubectl get replicaset`
- `kubeclt replace -f replica-set-def.yml  - update replica set`
- `kubeclt scale --replicas=6 -f repl.yml`
- `kubeclt scale --replicas=6 -f replicaset my-app`
- `kubectl get replicaSet new-replica-set -o yaml`

### Get api version 
- `kubectl explain replicaset | grep VERSION `


## Namespace
- `kubectl get pods --namespace kube-system`
- `kubectl get namespace`
- `kubectl get pods --all-namespaces`

## switch namespace
- `kubectl config set-context $(kubectl config current-context) --namespace=dev`

`
kubectl [command] [TYPE] [NAME] -o <output_format>
`

## Here are some of the commonly used formats:
- -o json Output a JSON formatted API object.
- -o name Print only the resource name and nothing else.
- -o wide Output in the plain-text format with any additional information.
- -o yaml Output a YAML formatted API object.
