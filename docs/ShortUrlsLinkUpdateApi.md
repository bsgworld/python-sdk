# bsg_api.ShortUrlsLinkUpdateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_link_update**](ShortUrlsLinkUpdateApi.md#short_urls_link_update) | **PUT** /api/short-url/links/{uuid} | Update short link |


# **short_urls_link_update**
> ShortUrlsLinkUpdate200Response short_urls_link_update(uuid, link_update_request)

Update short link

You can update short link name, slug or original link

**Please note:** If you change the original link to new one that hasn't been ever used before it may requires moderation
and short link status may be changed to *blocked*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.link_update_request import LinkUpdateRequest
from bsg_api.models.short_urls_link_update200_response import ShortUrlsLinkUpdate200Response
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
    api_instance = bsg_api.ShortUrlsLinkUpdateApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity
    link_update_request = {"name":"New name"} # LinkUpdateRequest | 

    try:
        # Update short link
        api_response = api_instance.short_urls_link_update(uuid, link_update_request)
        print("The response of ShortUrlsLinkUpdateApi->short_urls_link_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsLinkUpdateApi->short_urls_link_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |
| **link_update_request** | [**LinkUpdateRequest**](LinkUpdateRequest.md) |  |  |

### Return type

[**ShortUrlsLinkUpdate200Response**](ShortUrlsLinkUpdate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful updated |  -  |
| **422** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

