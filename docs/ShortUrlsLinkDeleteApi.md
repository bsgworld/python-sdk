# bsg_api.ShortUrlsLinkDeleteApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_link_delete**](ShortUrlsLinkDeleteApi.md#short_urls_link_delete) | **DELETE** /api/short-url/links/{uuid} | Remove short link |


# **short_urls_link_delete**
> object short_urls_link_delete(uuid)

Remove short link

If short link is *active* it will be *deleted*. Next few days this action can be reverted and link
may become *active* again. If short link already *blocked* or *deleted* it will be removed permanently. 


### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
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
    api_instance = bsg_api.ShortUrlsLinkDeleteApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity

    try:
        # Remove short link
        api_response = api_instance.short_urls_link_delete(uuid)
        print("The response of ShortUrlsLinkDeleteApi->short_urls_link_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsLinkDeleteApi->short_urls_link_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **204** | Successful removed |  -  |
| **422** | Short link not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

