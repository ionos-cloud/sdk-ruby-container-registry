# TokensApi

All URIs are relative to *https://api.ionos.com/containerregistries*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**registries_tokens_delete**](TokensApi.md#registries_tokens_delete) | **DELETE** /registries/{registryId}/tokens/{tokenId} | Delete token |
| [**registries_tokens_find_by_id**](TokensApi.md#registries_tokens_find_by_id) | **GET** /registries/{registryId}/tokens/{tokenId} | Get token information |
| [**registries_tokens_get**](TokensApi.md#registries_tokens_get) | **GET** /registries/{registryId}/tokens | List all tokens for the container registry |
| [**registries_tokens_patch**](TokensApi.md#registries_tokens_patch) | **PATCH** /registries/{registryId}/tokens/{tokenId} | Update token |
| [**registries_tokens_post**](TokensApi.md#registries_tokens_post) | **POST** /registries/{registryId}/tokens | Create token |
| [**registries_tokens_put**](TokensApi.md#registries_tokens_put) | **PUT** /registries/{registryId}/tokens/{tokenId} | Create or replace token |


## registries_tokens_delete

> registries_tokens_delete(registry_id, token_id)

Delete token

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

api_instance = IonoscloudContainerRegistry::TokensApi.new
registry_id = TODO # String | The unique ID of the registry
token_id = TODO # String | The unique ID of the token

begin
  # Delete token
  api_instance.registries_tokens_delete(registry_id, token_id)
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_delete: #{e}"
end
```

#### Using the registries_tokens_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> registries_tokens_delete_with_http_info(registry_id, token_id)

```ruby
begin
  # Delete token
  data, status_code, headers = api_instance.registries_tokens_delete_with_http_info(registry_id, token_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **token_id** | [**String**](.md) | The unique ID of the token |  |

### Return type

nil (empty response body)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registries_tokens_find_by_id

> <TokenResponse> registries_tokens_find_by_id(registry_id, token_id)

Get token information

Gets all information for a specific token used to access a container registry

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

api_instance = IonoscloudContainerRegistry::TokensApi.new
registry_id = TODO # String | The unique ID of the registry
token_id = TODO # String | The unique ID of the token

begin
  # Get token information
  result = api_instance.registries_tokens_find_by_id(registry_id, token_id)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_find_by_id: #{e}"
end
```

#### Using the registries_tokens_find_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TokenResponse>, Integer, Hash)> registries_tokens_find_by_id_with_http_info(registry_id, token_id)

```ruby
begin
  # Get token information
  data, status_code, headers = api_instance.registries_tokens_find_by_id_with_http_info(registry_id, token_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TokenResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_find_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **token_id** | [**String**](.md) | The unique ID of the token |  |

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registries_tokens_get

> <TokensResponse> registries_tokens_get(registry_id, opts)

List all tokens for the container registry

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

api_instance = IonoscloudContainerRegistry::TokensApi.new
registry_id = TODO # String | The unique ID of the registry
opts = {
  offset: 'offset_example', # String | The first element (from the complete list of the elements) to include in the response (used together with limit for pagination)
  limit: 'limit_example' # String | The maximum number of elements to return (used together with offset for pagination)
}

begin
  # List all tokens for the container registry
  result = api_instance.registries_tokens_get(registry_id, opts)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_get: #{e}"
end
```

#### Using the registries_tokens_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TokensResponse>, Integer, Hash)> registries_tokens_get_with_http_info(registry_id, opts)

```ruby
begin
  # List all tokens for the container registry
  data, status_code, headers = api_instance.registries_tokens_get_with_http_info(registry_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TokensResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **offset** | **String** | The first element (from the complete list of the elements) to include in the response (used together with limit for pagination) | [optional][default to &#39;0&#39;] |
| **limit** | **String** | The maximum number of elements to return (used together with offset for pagination) | [optional][default to &#39;100&#39;] |

### Return type

[**TokensResponse**](TokensResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## registries_tokens_patch

> <TokenResponse> registries_tokens_patch(registry_id, token_id, patch_token_input)

Update token

Update token properties, for example: - change status to 'enabled' or 'disabled' - change expiry date

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

api_instance = IonoscloudContainerRegistry::TokensApi.new
registry_id = TODO # String | The unique ID of the registry
token_id = TODO # String | The unique ID of the token
patch_token_input = IonoscloudContainerRegistry::PatchTokenInput.new # PatchTokenInput | 

begin
  # Update token
  result = api_instance.registries_tokens_patch(registry_id, token_id, patch_token_input)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_patch: #{e}"
end
```

#### Using the registries_tokens_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TokenResponse>, Integer, Hash)> registries_tokens_patch_with_http_info(registry_id, token_id, patch_token_input)

```ruby
begin
  # Update token
  data, status_code, headers = api_instance.registries_tokens_patch_with_http_info(registry_id, token_id, patch_token_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TokenResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **token_id** | [**String**](.md) | The unique ID of the token |  |
| **patch_token_input** | [**PatchTokenInput**](PatchTokenInput.md) |  |  |

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registries_tokens_post

> <PostTokenOutput> registries_tokens_post(registry_id, post_token_input)

Create token

Create a token - password is only available once in the POST response

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

api_instance = IonoscloudContainerRegistry::TokensApi.new
registry_id = TODO # String | The unique ID of the registry
post_token_input = IonoscloudContainerRegistry::PostTokenInput.new({properties: IonoscloudContainerRegistry::PostTokenProperties.new({name: 'push-token'})}) # PostTokenInput | 

begin
  # Create token
  result = api_instance.registries_tokens_post(registry_id, post_token_input)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_post: #{e}"
end
```

#### Using the registries_tokens_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostTokenOutput>, Integer, Hash)> registries_tokens_post_with_http_info(registry_id, post_token_input)

```ruby
begin
  # Create token
  data, status_code, headers = api_instance.registries_tokens_post_with_http_info(registry_id, post_token_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostTokenOutput>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **post_token_input** | [**PostTokenInput**](PostTokenInput.md) |  |  |

### Return type

[**PostTokenOutput**](PostTokenOutput.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## registries_tokens_put

> <PutTokenOutput> registries_tokens_put(registry_id, token_id, put_token_input)

Create or replace token

Create/replace a token - password is only available once in the create response - \"name\" cannot be changed

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

api_instance = IonoscloudContainerRegistry::TokensApi.new
registry_id = TODO # String | The unique ID of the registry
token_id = 'token_id_example' # String | The unique ID of the token
put_token_input = IonoscloudContainerRegistry::PutTokenInput.new({properties: IonoscloudContainerRegistry::PostTokenProperties.new({name: 'push-token'})}) # PutTokenInput | 

begin
  # Create or replace token
  result = api_instance.registries_tokens_put(registry_id, token_id, put_token_input)
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_put: #{e}"
end
```

#### Using the registries_tokens_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PutTokenOutput>, Integer, Hash)> registries_tokens_put_with_http_info(registry_id, token_id, put_token_input)

```ruby
begin
  # Create or replace token
  data, status_code, headers = api_instance.registries_tokens_put_with_http_info(registry_id, token_id, put_token_input)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PutTokenOutput>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling TokensApi->registries_tokens_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **registry_id** | [**String**](.md) | The unique ID of the registry |  |
| **token_id** | **String** | The unique ID of the token |  |
| **put_token_input** | [**PutTokenInput**](PutTokenInput.md) |  |  |

### Return type

[**PutTokenOutput**](PutTokenOutput.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

