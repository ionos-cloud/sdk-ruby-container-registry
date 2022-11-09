# PatchRegistryInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **garbage_collection_schedule** | [**WeeklySchedule**](WeeklySchedule.md) |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::PatchRegistryInput.new(
  garbage_collection_schedule: null
)
```

