# bsg_api.ShortUrlsLinkCreateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_link_create**](ShortUrlsLinkCreateApi.md#short_urls_link_create) | **POST** /api/short-url/links | Create short link |


# **short_urls_link_create**
> ShortUrlsLinkCreate201Response short_urls_link_create(link_store_request)

Create short link

Create a short link for original link.

**Please note:** *Response contains new link status. If original link is used at first time it may not pass the moderation automatically.
Be careful only link in **active** status can be used for redirect!*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.link_store_request import LinkStoreRequest
from bsg_api.models.short_urls_link_create201_response import ShortUrlsLinkCreate201Response
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
    api_instance = bsg_api.ShortUrlsLinkCreateApi(api_client)
    link_store_request = bsg_api.LinkStoreRequest() # LinkStoreRequest | 

    try:
        # Create short link
        api_response = api_instance.short_urls_link_create(link_store_request)
        print("The response of ShortUrlsLinkCreateApi->short_urls_link_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsLinkCreateApi->short_urls_link_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **link_store_request** | [**LinkStoreRequest**](LinkStoreRequest.md) |  |  |

### Return type

[**ShortUrlsLinkCreate201Response**](ShortUrlsLinkCreate201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

