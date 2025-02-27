# Services
    
> see https://aka.ms/autorest

This is the AutoRest configuration file for Services.



---
## Getting Started 
To build the SDK for Services, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information 
These are the global settings for the Services API.

``` yaml
openapi-type: arm
tag: package-2019-06
```

### Tag: package-2019-06

These settings apply only when `--tag=package-2019-06` is specified on the command line.

``` yaml $(tag) == 'package-2019-06'
input-file:
- Microsoft.WindowsIoT/stable/2019-06-01/WindowsIotServices.json
```

### Tag: package-2018-02-preview

These settings apply only when `--tag=package-2018-02-preview` is specified on the command line.

``` yaml $(tag) == 'package-2018-02-preview'
input-file:
- Microsoft.WindowsIoT/preview/2018-02-16-preview/WindowsIotServices.json
```

---
# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-powershell
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-python-track2
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-go-track2
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-ruby
    after_scripts:
      - bundle install && rake arm:regen_all_profiles['azure_mgmt_windowsiot']
  - repo: azure-cli-extensions
  - repo: azure-resource-manager-schemas
```

## C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  # last generated with AutoRest.1.0.0-Nightly20170129 from commit 19f63015ea5a8a0fc64b9d7e2cdfeac447d93eaf
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.WindowsIoT
  payload-flattening-threshold: 1
  output-folder: $(csharp-sdks-folder)/windowsiot/Microsoft.Azure.Management.WindowsIoT/src/Generated
  clear-output-folder: true
```

## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## TypeScript

See configuration in [readme.typescript.md](./readme.typescript.md)

## Java

See configuration in [readme.java.md](./readme.java.md)

## Ruby

See configuration in [readme.ruby.md](./readme.ruby.md)




## Terraform

These settings apply only when `--terraform` is specified on the command line.

``` yaml $(terraform)
terraform:
    cli-name: windowsiot
    azure_arm: true
    license_header: MICROSOFT_MIT_NO_VERSION
    payload_flattening_threshold: 2
    namespace: windowsiot
    package-name: windowsiot
    clear-output-folder: false
```
