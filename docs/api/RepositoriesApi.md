# RepositoriesApi

All URIs are relative to *https://api.ionos.com/containerregistries*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**registries_repositories_delete**](RepositoriesApi.md#registries_repositories_delete) | **DELETE** /registries/{registryId}/repositories/{name} | Delete repository |


## registries_repositories_delete

> registries_repositories_delete(registry_id, name)

Delete repository

Delete all repository contents    The registry V2 API allows manifests and blobs to be deleted individually but it is not possible to remove an entire repository.   This operation is provided for convenience

### Examples

```ruby
require 'time'
require 'ionoscloud-container-registry'
# setup authorization
IonoscloudContainerRegistry.configure do |config|
  # Configure HTTP basic authorization: basicAuth
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'

  # Configure API key authorization: tokenAuth
  config.api_key['Authorization'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['Authorization'] = 'Bearer'
end

api_instance = IonoscloudContainerRegistry::RepositoriesApi.new
registry_id = TODO # String | The unique ID of the registry
name = 'ubuntu' # String | The name of the repository

begin
  # Delete repository
  api_instance.registries_repositories_delete(registry_id, name)
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RepositoriesApi->registries_repositories_delete: #{e}"
end
```

#### Using the registries_repositories_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> registries_repositories_delete_with_http_info(registry_id, name)

```ruby
begin
  # Delete repository
  data, status_code, headers = api_instance.registries_repositories_delete_with_http_info(registry_id, name)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RepositoriesApi->registries_repositories_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **name** | **String** | The name of the repository |  |

### Return type

nil (empty response body)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

