# injection-test

## Description
Test package for the config injection of PackageVariant

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] injection-test`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree injection-test`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init injection-test
kpt live apply injection-test --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
