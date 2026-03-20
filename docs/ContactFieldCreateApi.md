# bsg_api.ContactFieldCreateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_field_create**](ContactFieldCreateApi.md#contact_field_create) | **POST** /api/contacts/fields | Create contact field |


# **contact_field_create**
> ContactFieldCreate201Response contact_field_create(contact_field_create_request)

Create contact field

The method allows the creation of additional custom fields for contacts

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_field_create201_response import ContactFieldCreate201Response
from bsg_api.models.contact_field_create_request import ContactFieldCreateRequest
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
    api_instance = bsg_api.ContactFieldCreateApi(api_client)
    contact_field_create_request = bsg_api.ContactFieldCreateRequest() # ContactFieldCreateRequest | 

    try:
        # Create contact field
        api_response = api_instance.contact_field_create(contact_field_create_request)
        print("The response of ContactFieldCreateApi->contact_field_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldCreateApi->contact_field_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_field_create_request** | [**ContactFieldCreateRequest**](ContactFieldCreateRequest.md) |  |  |

### Return type

[**ContactFieldCreate201Response**](ContactFieldCreate201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

