# bsg_api.ContactListUpdateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list_update**](ContactListUpdateApi.md#contact_list_update) | **PUT** /api/groups/{id} | Update list |


# **contact_list_update**
> ContactListUpdate200Response contact_list_update(id, contact_list_update_request)

Update list

Performs editing of the selected contacts list

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_update200_response import ContactListUpdate200Response
from bsg_api.models.contact_list_update_request import ContactListUpdateRequest
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
    api_instance = bsg_api.ContactListUpdateApi(api_client)
    id = 56 # int | 
    contact_list_update_request = bsg_api.ContactListUpdateRequest() # ContactListUpdateRequest | 

    try:
        # Update list
        api_response = api_instance.contact_list_update(id, contact_list_update_request)
        print("The response of ContactListUpdateApi->contact_list_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListUpdateApi->contact_list_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |
| **contact_list_update_request** | [**ContactListUpdateRequest**](ContactListUpdateRequest.md) |  |  |

### Return type

[**ContactListUpdate200Response**](ContactListUpdate200Response.md)

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

