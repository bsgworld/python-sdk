# bsg_api.StoplistAddApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**stoplist_add**](StoplistAddApi.md#stoplist_add) | **POST** /api/stoplist/attach | Add contacts to stop list |


# **stoplist_add**
> StoplistAdd200Response stoplist_add(stoplist_add_request)

Add contacts to stop list

Performs adding one or more contacts to the stop list

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.stoplist_add200_response import StoplistAdd200Response
from bsg_api.models.stoplist_add_request import StoplistAddRequest
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
    api_instance = bsg_api.StoplistAddApi(api_client)
    stoplist_add_request = bsg_api.StoplistAddRequest() # StoplistAddRequest | 

    try:
        # Add contacts to stop list
        api_response = api_instance.stoplist_add(stoplist_add_request)
        print("The response of StoplistAddApi->stoplist_add:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoplistAddApi->stoplist_add: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stoplist_add_request** | [**StoplistAddRequest**](StoplistAddRequest.md) |  |  |

### Return type

[**StoplistAdd200Response**](StoplistAdd200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful attached |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

