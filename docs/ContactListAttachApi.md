# bsg_api.ContactListAttachApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list_attach**](ContactListAttachApi.md#contact_list_attach) | **POST** /api/groups/attach | Add contacts to the list |


# **contact_list_attach**
> object contact_list_attach(contact_list_attach_request)

Add contacts to the list

The method provides the ability to add an existing contact to the list. The action can be single or bulk.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_attach_request import ContactListAttachRequest
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
    api_instance = bsg_api.ContactListAttachApi(api_client)
    contact_list_attach_request = {"contacts":[248452959,248452739,248452740],"groups":[1864623,1864621]} # ContactListAttachRequest | 

    try:
        # Add contacts to the list
        api_response = api_instance.contact_list_attach(contact_list_attach_request)
        print("The response of ContactListAttachApi->contact_list_attach:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListAttachApi->contact_list_attach: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_list_attach_request** | [**ContactListAttachRequest**](ContactListAttachRequest.md) |  |  |

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
| **200** | Successful attached |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

