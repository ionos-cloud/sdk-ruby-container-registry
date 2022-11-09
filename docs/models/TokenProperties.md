# TokenProperties

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credentials** | [**Credentials**](Credentials.md) |  |  |
| **expiry_date** | **Time** |  | [optional] |
| **name** | **String** |  |  |
| **scopes** | [**Array&lt;Scope&gt;**](Scope.md) |  | [optional] |
| **status** | **String** |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::TokenProperties.new(
  credentials: null,
  expiry_date: null,
  name: push-token,
  scopes: null,
  status: null
)
```

