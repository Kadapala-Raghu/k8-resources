$ kubectl get namespace # Viewing namespaces

# Setting the namespace for a request 

$ kubectl run nginx --image=nginx --namespace=<insert-namespace-name-here>
$ kubectl get pods --namespace=<insert-namespace-name-here>

# To delete resource

$ kubectl delete -f 01-namespace.yaml

$ $ kubectl apply -f 01-namespace.yaml

$ kubectl get namespaces

$ kubectl get pods -n expense # checking particular pod in Namespaces

$ kubectl describe pods multi-container # Check the background action play for the pods

$ kubectl exec -it multi-container -- bash # It will go inisde of the pod [ first pod ]

$ kubectl exec -it multi-container -c almalinux -- bash  # TO particular container

## Here all pods are sharing same IP and storage in K8

$ kubectl apply -f fie.yaml # create pods

$ kubectl top pod # Checking how much POD consuming the CPU 

$ kubectl get configmap # To view the config map

$ kubectl describe <resource-name> <container-name> # To view the any resource of container

$ echo -n "admin" | base64

$ echo "encrypt-string" | base64 --decode

$ kubectl describe Secret <secret-name-resource> 

$ kubectl delete pods --all -n default # Delete the all pods

$ kubectl get svc # View the services 

$ kubectl get pods -o wide # View the pod IP address 


### Session 49 March-05 -- 45:00 min daggara doubt 


$ kubectl get pods -o wide # View the in which IP is running that container 

$ kubectl get svc ## below IP is cluster IP

$ kubectl get pods -o wide # POds IP 