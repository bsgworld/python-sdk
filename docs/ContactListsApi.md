# bsg_api.ContactListsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_lists**](ContactListsApi.md#contact_lists) | **GET** /api/groups | List of contact lists |


# **contact_lists**
> ContactLists200Response contact_lists(page_offset=page_offset, page_limit=page_limit)

List of contact lists

Provides an index of all the contact lists with data

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_lists200_response import ContactLists200Response
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
    api_instance = bsg_api.ContactListsApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)

    try:
        # List of contact lists
        api_response = api_instance.contact_lists(page_offset=page_offset, page_limit=page_limit)
        print("The response of ContactListsApi->contact_lists:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListsApi->contact_lists: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |

### Return type

[**ContactLists200Response**](ContactLists200Response.md)

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

