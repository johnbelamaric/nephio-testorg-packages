# nephio-workload-cluster

## Description

Deploying this package to the Nephio management cluster will result in the
provisioning of a workload cluster, associated repository, tokens, secrets,
and other resources needed to fully register the new cluster with Nephio.

To accomplish this, the package will deploy two additional packages to the
management cluster: one for the cluster, and one for the repository. The names
of those packages will be based on the name of this package. So, if this package
is cloned to the name "cluster-01", it will deploy two additional packages,
"cluster-01-cluster", and "cluster-01-repo".
