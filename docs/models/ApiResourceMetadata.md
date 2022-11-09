# ApiResourceMetadata

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_by** | **String** |  |  |
| **created_by_user_id** | **String** |  |  |
| **created_date** | **Time** |  |  |
| **last_modified_by** | **String** |  | [optional] |
| **last_modified_by_user_id** | **String** |  | [optional] |
| **last_modified_date** | **Time** |  | [optional] |
| **state** | **String** |  |  |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::ApiResourceMetadata.new(
  created_by: null,
  created_by_user_id: null,
  created_date: null,
  last_modified_by: null,
  last_modified_by_user_id: null,
  last_modified_date: null,
  state: null
)
```

