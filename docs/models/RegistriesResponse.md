# RegistriesResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_links** | [**PaginationLinks**](PaginationLinks.md) |  |  |
| **href** | **String** |  | [optional] |
| **id** | **String** |  | [optional] |
| **items** | [**Array&lt;RegistryResponse&gt;**](RegistryResponse.md) |  | [optional] |
| **limit** | **Integer** |  |  |
| **next_page_token** | **String** |  |  |
| **type** | **String** |  | [optional] |

## Example

```ruby
require 'ionoscloud-container-registry'

instance = IonoscloudContainerRegistry::RegistriesResponse.new(
  _links: null,
  href: null,
  id: null,
  items: null,
  limit: null,
  next_page_token: null,
  type: null
)
```

