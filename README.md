# helm-charts

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```sh
helm repo add void-xmh https://xmh19936688.github.io/helm-charts
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
void-xmh` to see the charts.

To install chart, for example, `go-eg`:

```sh
helm install my-go-eg void-xmh/go-eg
```

To uninstall the chart:

```sh
helm delete my-go-eg
```

To show values can be customized:

```sh
helm show values void-xmh/go-eg
```
