# Scope

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **actions** | **Array&lt;String&gt;** |  |  |
| **name** | **String** |  |  |
| **type** | **String** |  |  |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::Scope.new(
  actions: ["pull", "push", "delete"],
  name: *,
  type: repository
)
```

