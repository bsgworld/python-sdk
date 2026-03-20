# bsg_api.StoplistItemsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**stoplist_items**](StoplistItemsApi.md#stoplist_items) | **GET** /api/stoplist | List the contacts of stop lists |


# **stoplist_items**
> StoplistItems200Response stoplist_items(page_offset=page_offset, page_limit=page_limit, type=type)

List the contacts of stop lists

The method allows getting a list of contacts that were added to the SMS and/or Viber stop list

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.stoplist_items200_response import StoplistItems200Response
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
    api_instance = bsg_api.StoplistItemsApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 20 # int | The number of items in the response (optional) (default to 20)
    type = 'type_example' # str | Specify the type of the stop list for which we need to return the contact list. If the stop list type is not specified, the method will return data for all the stop list types (optional)

    try:
        # List the contacts of stop lists
        api_response = api_instance.stoplist_items(page_offset=page_offset, page_limit=page_limit, type=type)
        print("The response of StoplistItemsApi->stoplist_items:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoplistItemsApi->stoplist_items: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 20] |
| **type** | **str** | Specify the type of the stop list for which we need to return the contact list. If the stop list type is not specified, the method will return data for all the stop list types | [optional]  |

### Return type

[**StoplistItems200Response**](StoplistItems200Response.md)

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

