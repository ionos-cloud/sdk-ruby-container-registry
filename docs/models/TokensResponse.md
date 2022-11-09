# TokensResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_links** | [**PaginationLinks**](PaginationLinks.md) |  |  |
| **count** | **Integer** |  |  |
| **href** | **String** |  | [optional] |
| **id** | **String** |  | [optional] |
| **items** | [**Array&lt;TokenResponse&gt;**](TokenResponse.md) |  | [optional] |
| **limit** | **Integer** |  |  |
| **offset** | **Integer** |  |  |
| **total** | **Integer** |  |  |
| **type** | **String** |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::TokensResponse.new(
  _links: null,
  count: null,
  href: null,
  id: null,
  items: null,
  limit: null,
  offset: null,
  total: null,
  type: null
)
```

