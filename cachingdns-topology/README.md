# cachingdns-topology

## Description
Deploys a multi-tiered, multi-cluster Caching DNS architecture based on CoreDNS.

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] cachingdns-topology`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree cachingdns-topology`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init cachingdns-topology
kpt live apply cachingdns-topology --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
