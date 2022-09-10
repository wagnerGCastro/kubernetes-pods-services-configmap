## Install Kubernet and Minikube

- Class (03) - Creating and Understanding Pods
  - Creating first can, entry in  directory class/03/1-first-pod.yaml:
  ``` bash
    $ kubectl apply -f ./1-first-pod.yaml
    $ kubectl get pods
    $ kubectl describe pod nginx-pod

    $ kubectl delete pod nginx-pod
    $ kubectl delete -f ./1-first-pod.yaml
  ```


- Class (03) - Creating and Understanding Pods
  - Creating news portal can, entry in  directory class/03/2-news-portal.yaml:
  ``` bash
    $ kubectl apply -f ./2-news-portal.yaml
    $ kubectl get pods
    $ kubectl describe pod news-portal
    $ kubectl exec -it news-portal bash bash
    $ kubectl exec -it news-portal bash -- bash
    
    $ kubectl delete pod news-portal
    $ kubectl delete -f ./2-news-portal.yaml
  ```
