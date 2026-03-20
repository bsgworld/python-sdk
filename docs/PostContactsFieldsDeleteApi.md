# bsg_api.PostContactsFieldsDeleteApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**post_contacts_fields_delete**](PostContactsFieldsDeleteApi.md#post_contacts_fields_delete) | **POST** /api/contacts/fields/delete | Delete contact fields by ids |


# **post_contacts_fields_delete**
> object post_contacts_fields_delete(post_contacts_fields_delete_request)

Delete contact fields by ids

Delete multiple (up to 30) contact fields

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.post_contacts_fields_delete_request import PostContactsFieldsDeleteRequest
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
    api_instance = bsg_api.PostContactsFieldsDeleteApi(api_client)
    post_contacts_fields_delete_request = bsg_api.PostContactsFieldsDeleteRequest() # PostContactsFieldsDeleteRequest | 

    try:
        # Delete contact fields by ids
        api_response = api_instance.post_contacts_fields_delete(post_contacts_fields_delete_request)
        print("The response of PostContactsFieldsDeleteApi->post_contacts_fields_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostContactsFieldsDeleteApi->post_contacts_fields_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_contacts_fields_delete_request** | [**PostContactsFieldsDeleteRequest**](PostContactsFieldsDeleteRequest.md) |  |  |

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
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

