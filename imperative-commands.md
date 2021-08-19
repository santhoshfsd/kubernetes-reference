### Deploy the pod
`kubectl run nginx-pod --image=nginx:alpine`

### Deploy a pod with label
#### run the following  command to generate the file
`kubectl run redis --image=redis:alpine --dry-run=client -oyaml > redis-pod.yaml`

### create service using command

`kubectl expose pod redis --port=6379 --name redis-service`

### create deployment 
`kubectl create deployment webapp --image=kodekloud/webapp-color --replicas=3`

### run the pod and expose the port 
`kubectl run custom-nginx --image=nginx --port=8080`

### create deployment with namespace
`kubectl create deployment redis-deploy --image=redis --replicas=2 -n dev-ns`

## Create a pod called httpd using the image httpd:alpine in the default namespace. Next, create a service of type ClusterIP by the same name (httpd). The target port for the service should 80

`kubectl run httpd --image=httpd:alpine --port=80 --expose`


### web ui dashboard
- The Dashboard UI is not deployed by default.

`kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.2.0/aio/deploy/recommended.yaml `

- command line proxy
` kubectl proxy `

- Get token
` https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md `

- `https://github.com/kubernetes/dashboard`

- ` kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"`