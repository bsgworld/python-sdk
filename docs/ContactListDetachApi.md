# bsg_api.ContactListDetachApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list_detach**](ContactListDetachApi.md#contact_list_detach) | **POST** /api/groups/detach | Remove contacts from the list |


# **contact_list_detach**
> object contact_list_detach(contact_list_detach_request)

Remove contacts from the list

Performs the removal of contact from the list. The action can be single (string) or bulk (array)

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_detach_request import ContactListDetachRequest
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
    api_instance = bsg_api.ContactListDetachApi(api_client)
    contact_list_detach_request = {"contacts":[248452959,248452739,248452740],"groups":[1864623,1864621]} # ContactListDetachRequest | 

    try:
        # Remove contacts from the list
        api_response = api_instance.contact_list_detach(contact_list_detach_request)
        print("The response of ContactListDetachApi->contact_list_detach:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListDetachApi->contact_list_detach: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_list_detach_request** | [**ContactListDetachRequest**](ContactListDetachRequest.md) |  |  |

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

