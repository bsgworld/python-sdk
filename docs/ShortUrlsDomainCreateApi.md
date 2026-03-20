# bsg_api.ShortUrlsDomainCreateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_domain_create**](ShortUrlsDomainCreateApi.md#short_urls_domain_create) | **POST** /api/short-url/domains | Add domain |


# **short_urls_domain_create**
> ShortUrlsDomainCreate201Response short_urls_domain_create(domain_store_request=domain_store_request)

Add domain

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.domain_store_request import DomainStoreRequest
from bsg_api.models.short_urls_domain_create201_response import ShortUrlsDomainCreate201Response
from bsg_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://one-api.bsg.world
# See configuration.py for a list of all supported configuration parameters.
configuration = bsg_api.Configuration(
    host = "https://one-api.bsg.world"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): ExternalAuth
configuration = bsg_api.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with bsg_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = bsg_api.ShortUrlsDomainCreateApi(api_client)
    domain_store_request = {"name":"short.ai","slug_type":"random"} # DomainStoreRequest |  (optional)

    try:
        # Add domain
        api_response = api_instance.short_urls_domain_create(domain_store_request=domain_store_request)
        print("The response of ShortUrlsDomainCreateApi->short_urls_domain_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsDomainCreateApi->short_urls_domain_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain_store_request** | [**DomainStoreRequest**](DomainStoreRequest.md) |  | [optional]  |

### Return type

[**ShortUrlsDomainCreate201Response**](ShortUrlsDomainCreate201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **422** | Error |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

