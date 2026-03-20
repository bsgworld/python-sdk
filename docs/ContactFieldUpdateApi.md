# bsg_api.ContactFieldUpdateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_field_update**](ContactFieldUpdateApi.md#contact_field_update) | **PATCH** /api/contacts/fields/{id} | Update contact field |


# **contact_field_update**
> ContactFieldUpdate200Response contact_field_update(id, contact_field_update_request)

Update contact field

Method for editing custom contact field:

- change field name
- change field description


### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_field_update200_response import ContactFieldUpdate200Response
from bsg_api.models.contact_field_update_request import ContactFieldUpdateRequest
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
    api_instance = bsg_api.ContactFieldUpdateApi(api_client)
    id = 56 # int | Contact field id
    contact_field_update_request = bsg_api.ContactFieldUpdateRequest() # ContactFieldUpdateRequest | 

    try:
        # Update contact field
        api_response = api_instance.contact_field_update(id, contact_field_update_request)
        print("The response of ContactFieldUpdateApi->contact_field_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldUpdateApi->contact_field_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact field id |  |
| **contact_field_update_request** | [**ContactFieldUpdateRequest**](ContactFieldUpdateRequest.md) |  |  |

### Return type

[**ContactFieldUpdate200Response**](ContactFieldUpdate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

