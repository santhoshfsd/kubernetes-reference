# kubernetes-reference

## kubectl commands
Set-Alias -Name k -value kubectl
### perform a trail create

- kubectl create -f pod-nginx-server.yml --dry-run --validate=true 

- Default values 
 --dry-run = client 
 --validate=true 

 ### apply changes

 - kubectl create -f pod-nginx-server.yml --save-config --record
 -save config 
    causes the resource config settings to be saved in the annotations
    save the initial state
 - kubectl describe pod [pod-name]
 - record 
   record the deployment command in the revision history

## Access the container in the pod
 - kubectl exec <pod-name> -it sh

 ## Resource limit
 https://stackoverflow.com/questions/64080471/kubernetes-one-or-more-containers-do-not-have-resource-limits-warning-in-vs-c

 ## memory limits
 https://www.alibabacloud.com/blog/kubernetes-assign-memory-resources-and-limits-to-containers_594830


 ## nginx
 port 80 - usr/share/nginx/html - index.html

 ## port forward to a random port
  kubectl port-forward deployment.apps/my-ngnix :80

  https://learnk8s.io/deploying-nodejs-kubernetes#defining-a-service


## create
  kubectl create -f .\nginx.deployment.yml --save-config --record


  ## logs init container pod
  kubectl logs  init-pod-demo -c init-app