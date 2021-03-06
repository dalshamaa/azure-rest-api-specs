## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: storagesync
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2018-07-01
  - tag: package-2018-04-02
```

### Tag: package-2018-07-01 and go

These settings apply only when `--tag=package-2018-07-01 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2018-07-01' && $(go)
output-folder: $(go-sdk-folder)/services/preview/storagesync/mgmt/2018-07-01/storagesync
```

### Tag: package-2018-04-02 and go

These settings apply only when `--tag=package-2018-04-02 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2018-04-02' && $(go)
output-folder: $(go-sdk-folder)/services/storagesync/mgmt/2018-04-02/storagesync
```
