# bsg_api.ShortUrlsDomainApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_domain**](ShortUrlsDomainApi.md#short_urls_domain) | **GET** /api/short-url/domains/{uuid} | Get domain by uuid |


# **short_urls_domain**
> ShortUrlsDomain200Response short_urls_domain(uuid)

Get domain by uuid

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_domain200_response import ShortUrlsDomain200Response
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
    api_instance = bsg_api.ShortUrlsDomainApi(api_client)
    uuid = 'db05af9e-107e-4ed6-b1ac-a373d90109c8' # str | Uuid of entity

    try:
        # Get domain by uuid
        api_response = api_instance.short_urls_domain(uuid)
        print("The response of ShortUrlsDomainApi->short_urls_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsDomainApi->short_urls_domain: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |

### Return type

[**ShortUrlsDomain200Response**](ShortUrlsDomain200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |
| **422** | Domain not found. Pass correct domain uuid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

