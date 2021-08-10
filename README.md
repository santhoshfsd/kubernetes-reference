# kubernetes-reference

## kubectl commands

### perform a trail create

- kubectl create -f pod-nginx-server.yml --dry-run --validate=true 

- Default values 
 --dry-run = client 
 --validate=true 

 ### apply changes

 - kubectl create -f pod-nginx-server.yml --save-config
 -save config 
    causes the resource config settings to be saved in the annotations
    save the initial state
 - kubectl describe pod [pod-name]

## Access the container in the pod
 - kubectl exec <pod-name> -it sh