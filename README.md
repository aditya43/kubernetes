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