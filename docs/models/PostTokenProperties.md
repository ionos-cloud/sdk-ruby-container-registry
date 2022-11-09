# PostTokenProperties

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **expiry_date** | **Time** |  | [optional] |
| **name** | **String** |  |  |
| **scopes** | [**Array&lt;Scope&gt;**](Scope.md) |  | [optional] |
| **status** | **String** |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::PostTokenProperties.new(
  expiry_date: null,
  name: push-token,
  scopes: null,
  status: null
)
```

