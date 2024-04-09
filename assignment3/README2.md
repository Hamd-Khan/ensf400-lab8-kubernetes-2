### Assignment 3 Instructions
## Hamd Khan 30143419


- Navigate to the Assignment3 Directory If you are not in it already. 

```bash
cd assignment3
```

- Then Run the Following Commands In Order:

```bash
minikube start
minikube addons enable ingress
kubectl apply -f '*.yaml'
curl http://$(minikube ip)/
```

Or You May Individually Run Each File:
```bash
kubectl apply -f nginx-dep.yaml
kubectl apply -f nginx-configmap.yaml
kubectl apply -f nginx-svc.yaml
kubectl apply -f nginx-ingress.yaml 
kubectl apply -f app-1-dep.yaml
kubectl apply -f app-1-svc.yaml
kubectl apply -f app-1-ingress.yaml
kubectl apply -f app-2-dep.yaml
kubectl apply -f app-2-svc.yaml
kubectl apply -f app-2-ingress.yaml
```


Once You have Ran One of These Two Methods You should see an output similar to this (if using method1 ):
![image]()

Here Is An Example of The Curl Command Running
![image]()

Here Is the output showcasing the deployments active while the command is running
![image]()

Here is the output showcasing the `kubectl get all command`
![image]()


If you are having troubles with the initial set up or configuration you can run the following and then rerun the commands at the start

```bash
minikube delete
```

If you are done with the program enter to delete the cluster:
```bash
minikube delete
```