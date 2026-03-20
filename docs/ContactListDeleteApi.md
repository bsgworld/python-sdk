# bsg_api.ContactListDeleteApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list_delete**](ContactListDeleteApi.md#contact_list_delete) | **DELETE** /api/groups/{id} | Delete list |


# **contact_list_delete**
> contact_list_delete(id)

Delete list

Method for deleting contact list. Please note that when you delete a contact list, all contacts that were added to it are not deleted from your Contact Book

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
    api_instance = bsg_api.ContactListDeleteApi(api_client)
    id = 56 # int | 

    try:
        # Delete list
        api_instance.contact_list_delete(id)
    except Exception as e:
        print("Exception when calling ContactListDeleteApi->contact_list_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |

### Return type

void (empty response body)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

