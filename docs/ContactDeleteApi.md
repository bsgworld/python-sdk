# bsg_api.ContactDeleteApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_delete**](ContactDeleteApi.md#contact_delete) | **DELETE** /api/contacts/{id} | Delete contact |


# **contact_delete**
> object contact_delete(id)

Delete contact

Use this query to remove an existing contact from the Contact Book. When this query is made, the contact will also be removed from all lists where it was added.

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
    api_instance = bsg_api.ContactDeleteApi(api_client)
    id = 56 # int | Contact id

    try:
        # Delete contact
        api_response = api_instance.contact_delete(id)
        print("The response of ContactDeleteApi->contact_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactDeleteApi->contact_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact id |  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

