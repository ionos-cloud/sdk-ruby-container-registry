# RegistryProperties

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **garbage_collection_schedule** | [**WeeklySchedule**](WeeklySchedule.md) |  | [optional] |
| **hostname** | **String** |  | [optional] |
| **location** | **String** |  |  |
| **name** | **String** |  |  |
| **storage_usage** | [**StorageUsage**](StorageUsage.md) |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::RegistryProperties.new(
  garbage_collection_schedule: null,
  hostname: my-registry.cr.ionos.com,
  location: de/txl,
  name: my-registry,
  storage_usage: null
)
```

