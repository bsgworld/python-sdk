# bsg_api.ContactsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contacts**](ContactsApi.md#contacts) | **GET** /api/contacts | List of contacts |


# **contacts**
> Contacts200Response contacts(page_offset=page_offset, page_limit=page_limit, groups=groups)

List of contacts

Get a list of existing contacts in the Contact Book of your account with detailed information on each of them. The method also allows you to get contacts from the certain lists that you specified in the query parameters.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contacts200_response import Contacts200Response
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
    api_instance = bsg_api.ContactsApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 20 # int | The number of items in the response (optional) (default to 20)
    groups = [[1864618]] # List[int] | Index of IDs of the lists for which you want to display contacts (optional)

    try:
        # List of contacts
        api_response = api_instance.contacts(page_offset=page_offset, page_limit=page_limit, groups=groups)
        print("The response of ContactsApi->contacts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsApi->contacts: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 20] |
| **groups** | [**List[int]**](int.md) | Index of IDs of the lists for which you want to display contacts | [optional]  |

### Return type

[**Contacts200Response**](Contacts200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Paginated list of contacts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

