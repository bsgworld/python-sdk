# bsg_api.ContactFieldsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_fields**](ContactFieldsApi.md#contact_fields) | **GET** /api/contacts/fields | List of contact fields |


# **contact_fields**
> ContactFieldCollectionSchema contact_fields()

List of contact fields

Get a list of custom fields

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_field_collection_schema import ContactFieldCollectionSchema
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
    api_instance = bsg_api.ContactFieldsApi(api_client)

    try:
        # List of contact fields
        api_response = api_instance.contact_fields()
        print("The response of ContactFieldsApi->contact_fields:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldsApi->contact_fields: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ContactFieldCollectionSchema**](ContactFieldCollectionSchema.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Contact field list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

