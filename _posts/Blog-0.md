---
title: Blog 0
layout: post
category: Blog
toc_level: 1
date: 2020-1-31
---

So for this week blog I decided to learn what kubernet is  adn what it can do. In simple temrs  its a  open soucre platform that  can automates for  linux operations. It was really cool to use the this tool called Minikube wihic allows you to run the kubernetes virtual with out have to downlaod the software. This is laos wiht the help of  katakoda which power the VM for minikube. So what I tired to deploy a simple  Hello world Node.js app. Once kube  has started  there is set command that  to deploy the a pod which runs a docker file.

kubectl create deployment hello-node --image=gcr.io/hello-minikube-zero-install/hello-node

This command strats pod, sto which can use this commmand to see that its runnning:

kubectl get pods

We then go to actually change the ports on  this pod to  because it order to be exposed for this cluster  it need this command:

kubectl expose deployment hello-node --type=LoadBalancer --port=8080

The part of the command that allows for this cluster to be exposed to the outsde is from this piece of code --type=Loadbalancer. We then run the following command to luach the services of the pod to run its applciaiotn:

minikube service hello-node

This will show  apllaciotn through the load blance with the help of  the minikube service.

you then will get the reuslt of this web page:

![Hello Wolrd!](/assets/img/Hello.jpg)



This is the Hello Wolrd ! Training Lab
