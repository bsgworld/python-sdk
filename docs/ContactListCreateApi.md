# bsg_api.ContactListCreateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list_create**](ContactListCreateApi.md#contact_list_create) | **POST** /api/groups | Create list |


# **contact_list_create**
> ContactListCreate201Response contact_list_create(contact_list_create_request)

Create list

Create a contact list to group contacts

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_create201_response import ContactListCreate201Response
from bsg_api.models.contact_list_create_request import ContactListCreateRequest
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
    api_instance = bsg_api.ContactListCreateApi(api_client)
    contact_list_create_request = {"name":"new list 123"} # ContactListCreateRequest | 

    try:
        # Create list
        api_response = api_instance.contact_list_create(contact_list_create_request)
        print("The response of ContactListCreateApi->contact_list_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListCreateApi->contact_list_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_list_create_request** | [**ContactListCreateRequest**](ContactListCreateRequest.md) |  |  |

### Return type

[**ContactListCreate201Response**](ContactListCreate201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **422** | Error |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

