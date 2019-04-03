# KPF (Kube Port Forward)

## What is KPF?

KPF is a tool to assist in port redirects made through port-forward kubectl, keeping the current state and giving it a more refined control, being able to even save a state of several active redirects and restore them later, among other functions.

## Getting started

### Required dependencies

- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [jq](https://stedolan.github.io/jq/)

### Install KPF

```sh
$ curl -L https://github.com/supermock/kpf/releases/download/v1.0/kpf -o /usr/local/bin/kpf
$ chmod +x /usr/local/bin/kpf
```

### Some examples

Adding a port forward

```sh
# In this example I am adding a port forward to the Kubernetes Dashboard
$ kpf add kube-system k8s-app=kubernetes-dashboard 8443
```

Listing port forwards

```sh
$ kpf list
```

Removing a port forward

```sh
$ kpf del kube-system k8s-app=kubernetes-dashboard
```

For more examples, see the help...

## License

MIT