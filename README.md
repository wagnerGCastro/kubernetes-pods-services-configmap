## Install Kubernet and Minikube
  
( 2- ) Inicie seu cluster
  ver drivers: https://minikube.sigs.k8s.io/docs/drivers/vmware/
  $ minikube start --memory=2048mb --cpus=2 --driver=docker  ** para vmware
  $ minikube config set driver docker



  - 1)  para instalar docker machine
    - $ minikube start --memory=2048mb --cpus=2 --driver=vmware

    - https://access.redhat.com/documentation/en-us/red_hat_container_development_kit/3.0/html/installation_guide/docker-machine-driver-install

    $ sudo curl -L https://github.com/dhiltgen/docker-machine-kvm/releases/download/v0.7.0/docker-machine-driver-kvm -o /usr/local/bin/docker-machine-driver-kvm

    $ sudo chmod +x /usr/local/bin/docker-machine-driver-kvm



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


- Class (04) - Creating and Understanding Pods

  - Creating news portal can, entry in  directory class/03/2-news-portal.yaml:
  ``` bash
    $ kubectl apply -f ./2-news-portal.yaml
    $ kubectl get pods
    $ kubectl describe pod news-portal
    $ kubectl exec -it news-portal bash bash
    $ kubectl exec -it news-portal bash -- bash
    $ kubectl get pods -o wide

    -- before create service
    $  kubectl get services | kubectl get svc

    $ kubectl delete pod news-portal
    $ kubectl delete -f ./2-news-portal.yaml
  ```

- Class (05) - Creating Services, Pods, 

  - Creating namespaces to Pods and Services
  ``` bash
    $ kubectl apply -f ./news-portal-pod.yaml
    $ kubectl apply -f ./news-portal-service.yaml
    $ kubectl apply -f ./sistema-noticias-namespace.yaml
    $ kubectl apply -f ./sistema-noticias-pod.yaml
    $ kubectl apply -f ./sistema-noticias-service.yaml

    $ kubectl get services --namespace=sistema-noticias-namespace  -o wide 
    $ kubectl get pods --namespace=sistema-noticias-namespace  -o wide 
  ```
