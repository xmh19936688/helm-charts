# go-dev

Use for debugging go code inner pod on kubernetes.

## require

- Running kubernetes. Can be launched by kubeadm or minikube.
- `helm` installed. 

## usage

- Select one node and a path on it then clone your code.
- Install go-dev with helm.

You can install it online:

```sh
helm repo add void-xmh https://xmh19936688.github.io/helm-charts
NodeName=node CodePath=/path/to/code && \
helm install my-go-dev void-xmh/go-dev \
  -n my-go-dev \
  --create-namespace \
  --set nodeName=${NodeName} \
  --set codePath=${CodePath}
```

or from source code:

```sh
NodeName=node \
CodePath=/path/to/code && \
helm install my-go-dev . \
  -n my-go-dev \
  --create-namespace \
  --set nodeName=${NodeName} \
  --set codePath=${CodePath}
```

- Run `kube exec` into your go-dev pod and run commands as your IDE prompt.
- Enjoy & have fun!
