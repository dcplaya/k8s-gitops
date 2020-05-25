# GitOps workflow for kubernetes cluster

![](https://i.imgur.com/9tvyWMp.png)

Leverage [Flux](https://github.com/fluxcd/flux) to automate cluster state using code residing in this repo

## Setup

See [ansible/README.md](ansible/README.md) for more details.

## Workloads (by namespace)

* [cert-manager](cert-manager/)
* [default](default/)
* [flux](flux/)
* [kube-system](kube-system/)
* [logs](logs/)
* [monitoring](monitoring/)
* [rook-ceph](rook-ceph/)
* [system-upgrade](system-upgrade/)
* [velero](velero/)
