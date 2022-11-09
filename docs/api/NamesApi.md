# NamesApi

All URIs are relative to *https://api.ionos.com/containerregistries*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**names_check_usage**](NamesApi.md#names_check_usage) | **HEAD** /names/{name} | Get container registry name availability |


## names_check_usage

> names_check_usage(name)

Get container registry name availability

Validate that the name is suitable to use for a new registry: - it uses only the characters \"a-z\", \"0-9\", or \"-\" - and starts with a letter and ends with a letter or number - and is between 3 to 63 characters in length - and is available

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

api_instance = IonoscloudContainerRegistry::NamesApi.new
name = 'name_example' # String | The desired registry name

begin
  # Get container registry name availability
  api_instance.names_check_usage(name)
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling NamesApi->names_check_usage: #{e}"
end
```

#### Using the names_check_usage_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> names_check_usage_with_http_info(name)

```ruby
begin
  # Get container registry name availability
  data, status_code, headers = api_instance.names_check_usage_with_http_info(name)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling NamesApi->names_check_usage_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The desired registry name |  |

### Return type

nil (empty response body)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

