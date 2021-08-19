### commands

- kubectl get pod -o yaml
- kubectl describe pod podname
- kubectl exec podname -it sh

- kubectl logs podname -c container-name
- kubectl logs -p podname // previously run
- kubectl logs -f podname // stream logs


https://blog.codewithdan.com/4-kubectl-commands-to-help-debug-pod-issues-in-kubernetes/