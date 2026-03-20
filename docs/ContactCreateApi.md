# bsg_api.ContactCreateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_create**](ContactCreateApi.md#contact_create) | **POST** /api/contacts | Create a contact |


# **contact_create**
> ContactCreate201Response contact_create(store_contact)

Create a contact

The method allows adding new contacts to your Contact Book. 

**Please note:** that in the TEST account mode there is a restriction for performing this method: it is possible to create a contact only for a verified phone number (number verification is performed in the personal account of the platform).

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_create201_response import ContactCreate201Response
from bsg_api.models.store_contact import StoreContact
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
    api_instance = bsg_api.ContactCreateApi(api_client)
    store_contact = {"phone":61401629754} # StoreContact | 

    try:
        # Create a contact
        api_response = api_instance.contact_create(store_contact)
        print("The response of ContactCreateApi->contact_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactCreateApi->contact_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_contact** | [**StoreContact**](StoreContact.md) |  |  |

### Return type

[**ContactCreate201Response**](ContactCreate201Response.md)

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

