# bsg_api.ShortUrlsLinksApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_links**](ShortUrlsLinksApi.md#short_urls_links) | **GET** /api/short-url/links | List of short links |


# **short_urls_links**
> ShortUrlsLinks200Response short_urls_links(var_from, to, page=page, per_page=per_page)

List of short links

List of all created short links of selected period *from* to *to* with pagination by *per_page*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_links200_response import ShortUrlsLinks200Response
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
    api_instance = bsg_api.ShortUrlsLinksApi(api_client)
    var_from = '2022-04-28' # str | From date
    to = '2022-04-28' # str | To date
    page = 1 # int | Get items starting from this page. (optional) (default to 1)
    per_page = 20 # int | The number of items in the page. Possible values are from 10 to 500. (optional) (default to 20)

    try:
        # List of short links
        api_response = api_instance.short_urls_links(var_from, to, page=page, per_page=per_page)
        print("The response of ShortUrlsLinksApi->short_urls_links:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortUrlsLinksApi->short_urls_links: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_from** | **str** | From date |  |
| **to** | **str** | To date |  |
| **page** | **int** | Get items starting from this page. | [optional] [default to 1] |
| **per_page** | **int** | The number of items in the page. Possible values are from 10 to 500. | [optional] [default to 20] |

### Return type

[**ShortUrlsLinks200Response**](ShortUrlsLinks200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

