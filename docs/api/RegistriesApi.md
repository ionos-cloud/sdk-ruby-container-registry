# RegistriesApi

All URIs are relative to *https://api.ionos.com/containerregistries*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**registries_delete**](RegistriesApi.md#registries_delete) | **DELETE** /registries/{registryId} | Delete registry |
| [**registries_find_by_id**](RegistriesApi.md#registries_find_by_id) | **GET** /registries/{registryId} | Get a registry |
| [**registries_get**](RegistriesApi.md#registries_get) | **GET** /registries | List all container registries |
| [**registries_patch**](RegistriesApi.md#registries_patch) | **PATCH** /registries/{registryId} | Update the properties of a registry |
| [**registries_post**](RegistriesApi.md#registries_post) | **POST** /registries | Create container registry |
| [**registries_put**](RegistriesApi.md#registries_put) | **PUT** /registries/{registryId} | Create or replace a container registry |


## registries_delete

> registries_delete(registry_id)

Delete registry

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

api_instance = IonoscloudContainerRegistry::RegistriesApi.new
registry_id = TODO # String | The unique ID of the registry

begin
  # Delete registry
  api_instance.registries_delete(registry_id)
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_delete: #{e}"
end
```

#### Using the registries_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> registries_delete_with_http_info(registry_id)

```ruby
begin
  # Delete registry
  data, status_code, headers = api_instance.registries_delete_with_http_info(registry_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |

### Return type

nil (empty response body)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registries_find_by_id

> <RegistryResponse> registries_find_by_id(registry_id)

Get a registry

Get all information for a specific container registry

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

api_instance = IonoscloudContainerRegistry::RegistriesApi.new
registry_id = TODO # String | The unique ID of the registry

begin
  # Get a registry
  result = api_instance.registries_find_by_id(registry_id)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_find_by_id: #{e}"
end
```

#### Using the registries_find_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RegistryResponse>, Integer, Hash)> registries_find_by_id_with_http_info(registry_id)

```ruby
begin
  # Get a registry
  data, status_code, headers = api_instance.registries_find_by_id_with_http_info(registry_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RegistryResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_find_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |

### Return type

[**RegistryResponse**](RegistryResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registries_get

> <RegistriesResponse> registries_get(opts)

List all container registries

List all managed container registries for your account

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

api_instance = IonoscloudContainerRegistry::RegistriesApi.new
opts = {
  filter_name: 'my-registry', # String | The registry name to search for
  limit: 'limit_example', # String | The maximum number of elements to return (used together with nextPageToken for pagination)
  next_page_token: 'next_page_token_example' # String | The next page from the complete list of elements (used together with limit for pagination)
}

begin
  # List all container registries
  result = api_instance.registries_get(opts)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_get: #{e}"
end
```

#### Using the registries_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RegistriesResponse>, Integer, Hash)> registries_get_with_http_info(opts)

```ruby
begin
  # List all container registries
  data, status_code, headers = api_instance.registries_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RegistriesResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filter_name** | **String** | The registry name to search for | [optional] |
| **limit** | **String** | The maximum number of elements to return (used together with nextPageToken for pagination) | [optional][default to &#39;100&#39;] |
| **next_page_token** | **String** | The next page from the complete list of elements (used together with limit for pagination) | [optional] |

### Return type

[**RegistriesResponse**](RegistriesResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registries_patch

> <RegistryResponse> registries_patch(registry_id, patch_registry_input)

Update the properties of a registry

Update the properties of a registry - \"garbageCollectionSchedule\" time and days of the week for runs

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

api_instance = IonoscloudContainerRegistry::RegistriesApi.new
registry_id = TODO # String | The unique ID of the registry
patch_registry_input = IonoscloudContainerRegistry::PatchRegistryInput.new # PatchRegistryInput | 

begin
  # Update the properties of a registry
  result = api_instance.registries_patch(registry_id, patch_registry_input)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_patch: #{e}"
end
```

#### Using the registries_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RegistryResponse>, Integer, Hash)> registries_patch_with_http_info(registry_id, patch_registry_input)

```ruby
begin
  # Update the properties of a registry
  data, status_code, headers = api_instance.registries_patch_with_http_info(registry_id, patch_registry_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RegistryResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **patch_registry_input** | [**PatchRegistryInput**](PatchRegistryInput.md) |  |  |

### Return type

[**RegistryResponse**](RegistryResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registries_post

> <PostRegistryOutput> registries_post(post_registry_input)

Create container registry

Create a registry to hold container images or OCI compliant artifacts - \"name\" must have passed validation - \"location\" must be one of the available location IDs - \"garbageCollectionSchedule\" time and days of the week for runs

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

api_instance = IonoscloudContainerRegistry::RegistriesApi.new
post_registry_input = IonoscloudContainerRegistry::PostRegistryInput.new({properties: IonoscloudContainerRegistry::PostRegistryProperties.new({location: 'de/txl', name: 'my-registry'})}) # PostRegistryInput | 

begin
  # Create container registry
  result = api_instance.registries_post(post_registry_input)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_post: #{e}"
end
```

#### Using the registries_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostRegistryOutput>, Integer, Hash)> registries_post_with_http_info(post_registry_input)

```ruby
begin
  # Create container registry
  data, status_code, headers = api_instance.registries_post_with_http_info(post_registry_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostRegistryOutput>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_registry_input** | [**PostRegistryInput**](PostRegistryInput.md) |  |  |

### Return type

[**PostRegistryOutput**](PostRegistryOutput.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registries_put

> <PutRegistryOutput> registries_put(registry_id, put_registry_input)

Create or replace a container registry

Create/replace a registry to hold container images or OCI compliant artifacts  **On create** - \"name\" must have passed validation - \"location\" must be one of the available location IDs  **On update** - \"name\" cannot be changed - \"location\" cannot be changed  **On create or update** - \"garbageCollectionSchedule\": time and days of the week for runs 

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

api_instance = IonoscloudContainerRegistry::RegistriesApi.new
registry_id = TODO # String | The unique ID of the registry
put_registry_input = IonoscloudContainerRegistry::PutRegistryInput.new({properties: IonoscloudContainerRegistry::PostRegistryProperties.new({location: 'de/txl', name: 'my-registry'})}) # PutRegistryInput | 

begin
  # Create or replace a container registry
  result = api_instance.registries_put(registry_id, put_registry_input)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_put: #{e}"
end
```

#### Using the registries_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PutRegistryOutput>, Integer, Hash)> registries_put_with_http_info(registry_id, put_registry_input)

```ruby
begin
  # Create or replace a container registry
  data, status_code, headers = api_instance.registries_put_with_http_info(registry_id, put_registry_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PutRegistryOutput>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling RegistriesApi->registries_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **put_registry_input** | [**PutRegistryInput**](PutRegistryInput.md) |  |  |

### Return type

[**PutRegistryOutput**](PutRegistryOutput.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

