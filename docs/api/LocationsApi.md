# LocationsApi

All URIs are relative to *https://api.ionos.com/containerregistries*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**locations_get**](LocationsApi.md#locations_get) | **GET** /locations | Get container registry locations |


## locations_get

> <LocationsResponse> locations_get

Get container registry locations

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

api_instance = IonoscloudContainerRegistry::LocationsApi.new

begin
  # Get container registry locations
  result = api_instance.locations_get
  p result
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling LocationsApi->locations_get: #{e}"
end
```

#### Using the locations_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LocationsResponse>, Integer, Hash)> locations_get_with_http_info

```ruby
begin
  # Get container registry locations
  data, status_code, headers = api_instance.locations_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LocationsResponse>
rescue IonoscloudContainerRegistry::ApiError => e
  puts "Error when calling LocationsApi->locations_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**LocationsResponse**](LocationsResponse.md)

### Authorization

basicAuth, tokenAuth

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

