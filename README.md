## Kubernetes :anchor:
My personal notes, projects and configurations.

## Author
Aditya Hajare ([Linkedin](https://in.linkedin.com/in/aditya-hajare)).

## Current Status
WIP (Work In Progress)!

## License
Open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

----------------------------------------

## Important Notes
- [Local Setup On Mac](#local-setup-on-mac)
    ```diff
    + Setup Minikube
    + Verify Installation
    + Production Cluster
    ```
- [Cloud Setup](#cloud-setup)
    ```diff
    + Setup Kubernetes on AWS with kops
    ```

----------------------------------------

## Local Setup On Mac
```diff
+ Setup Minikube
```
- Install Virtualbox: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
- Install Minikube: [https://kubernetes.io/docs/tasks/tools/install-minikube/](https://kubernetes.io/docs/tasks/tools/install-minikube/)
- Execute:
    ```sh
    sudo mv minikube /usr/local/bin
    minikube start --driver=virtualbox
    ```
- Download and install `Kubectl`: [https://kubernetes.io/docs/tasks/tools/install-kubectl/](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

----------------------------------------

```diff
+ Verify Installation
```
- It sets up following config:
```sh
~/.kube/config

# View local cluster config:
cat ~/.kube/config
```

----------------------------------------

```diff
+ Production Cluster
```
- `kops` and `kubeadm` are tools to spin up a production cluster.
- With `AWS EKS` which is a hosted solution, we don't need to maintain the `masters`.
- On AWS, if we dont want to use `AWS EKS`, then the best tool after `EKS` is `kops`.
- With `kops`, we own all the infrastructure, so we also need to maintain the `masters`.
- `Kubeadm` is an alternative approach, `kops` is still recommended (on AWS) - because we also get AWS integrations (IAM, Load Balancer etc..) with `kops` automatically.
- `Kubeadm` is more of a generic tool. It is used more on DigitalOcean or bare metal setup.

----------------------------------------

## Cloud Setup
```diff
+ Setup Kubernetes on AWS with kops
```
- `kops` stands for `kubernetes operations`.
- `kops` allows us to create, destroy, upgrade and maintain production-grade, highly available, Kubernetes clusters from the command line.
- There is also a legacy tool called `kube-up.sh`. It has been deprecated and it doesn't create a production ready environment.
- `kops` only works on `Mac` and `Linux`.
- On `Windows`, we have to do following:
    * Download and install Virtualbox from: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
    * Download and install Vagrant from: [https://www.vagrantup.com/](https://www.vagrantup.com/)
    * To bootup a new linux VM, execute following in cmd/poweshell:
    ```sh
    C:\mkdir ubuntu
    C:\cd ubuntu
    C:\ubuntu>vagrant init ubuntu/xenial64
    C:\ubuntu>vagrant up
    ```
- Deployment guides: [https://kops.sigs.k8s.io/getting_started/install/](https://kops.sigs.k8s.io/getting_started/install/)

----------------------------------------