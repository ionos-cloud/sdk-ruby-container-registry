# WeeklySchedule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **days** | [**Array&lt;Day&gt;**](Day.md) |  |  |
| **time** | **String** | UTC time of day e.g. 01:00:00 - as defined by partial-time - RFC3339 |  |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::WeeklySchedule.new(
  days: null,
  time: 01:23:00+00:00
)
```

