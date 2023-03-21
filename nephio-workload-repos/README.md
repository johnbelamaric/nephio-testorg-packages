# nephio-workload-repos

## Description
Creates a workload cluster repository and registration with Nephio. This
package is intended for generating data for test/dev environments, not for a
real Nephio installation.

## Usage

When getting this package `--for-deployment`, the expectation is that the name
will be used to set the region, site, and site type labels. The name should be
of the form: `<env>-<region>-<site-type>-<cluster-number>`. For example, if
you clone this package to `myname-us-central1-edge-01`, then it will:
- Create a GH Repository resource resulting in a GitHub repository
  https://github.com/nephio-test/myname-us-central1-edge-01.git
- Create a Porch Repository resource to register that GH repository, with
  labels:
  - `kpt.dev/deployment-environment: production`  - this is static
  - `nephio.org/region: us-central1` - derived from the name
  - `nephio.org/site-type: edge` - derived from the name
  - `nephio.org/site: us-central1-edge-01` - derived from the name
- The Porch repository will have the name
  `<region>-<site-type>-<cluster-number>`; in other words, `<env>` is omitted,
  it is intended to be your name or GitHub handle or the test environment name.
  This allows many repos to co-exist in the nephio-test GitHub account.

Note that region MUST be `<string>-<string>`; the logic is all based on the `-`
delimiter.
