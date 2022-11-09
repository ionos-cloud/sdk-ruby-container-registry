# PatchTokenInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **expiry_date** | **Time** |  | [optional] |
| **scopes** | [**Array&lt;Scope&gt;**](Scope.md) |  | [optional] |
| **status** | **String** |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::PatchTokenInput.new(
  expiry_date: null,
  scopes: null,
  status: null
)
```

