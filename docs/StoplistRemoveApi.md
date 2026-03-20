# bsg_api.StoplistRemoveApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**stoplist_remove**](StoplistRemoveApi.md#stoplist_remove) | **POST** /api/stoplist/detach | Remove contacts from stop list |


# **stoplist_remove**
> object stoplist_remove(stoplist_remove_request)

Remove contacts from stop list

Performs the removal of one or more contacts from the stop list

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.stoplist_remove_request import StoplistRemoveRequest
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
    api_instance = bsg_api.StoplistRemoveApi(api_client)
    stoplist_remove_request = bsg_api.StoplistRemoveRequest() # StoplistRemoveRequest | 

    try:
        # Remove contacts from stop list
        api_response = api_instance.stoplist_remove(stoplist_remove_request)
        print("The response of StoplistRemoveApi->stoplist_remove:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StoplistRemoveApi->stoplist_remove: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stoplist_remove_request** | [**StoplistRemoveRequest**](StoplistRemoveRequest.md) |  |  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful detached |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

