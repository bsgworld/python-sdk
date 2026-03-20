# bsg_api.ShortUrlsLinkApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_link**](ShortUrlsLinkApi.md#short_urls_link) | **GET** /api/short-url/links/{uuid}/statistics | Get short link statistic |


# **short_urls_link**
> ShortUrlsLink200Response short_urls_link(uuid)

Get short link statistic

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_link200_response import ShortUrlsLink200Response
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
    api_instance = bsg_api.ShortUrlsLinkApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity

    try:
        # Get short link statistic
        api_response = api_instance.short_urls_link(uuid)
        print("The response of ShortUrlsLinkApi->short_urls_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsLinkApi->short_urls_link: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |

### Return type

[**ShortUrlsLink200Response**](ShortUrlsLink200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Short link statistic |  -  |
| **404** | Short link not found. Pass correct link uuid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

