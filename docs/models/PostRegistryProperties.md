# PostRegistryProperties

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **garbage_collection_schedule** | [**WeeklySchedule**](WeeklySchedule.md) |  | [optional] |
| **location** | **String** |  |  |
| **name** | **String** |  |  |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::PostRegistryProperties.new(
  garbage_collection_schedule: null,
  location: de/txl,
  name: my-registry
)
```

