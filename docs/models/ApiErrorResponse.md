# ApiErrorResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **http_status** | **Integer** |  |  |
| **messages** | [**Array&lt;ApiErrorMessage&gt;**](ApiErrorMessage.md) |  |  |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::ApiErrorResponse.new(
  http_status: 400,
  messages: null
)
```

