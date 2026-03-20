# bsg_api.ContactUpdateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_update**](ContactUpdateApi.md#contact_update) | **PUT** /api/contacts/{id} | Update contact |


# **contact_update**
> ContactUpdate200Response contact_update(id, contact_update_request)

Update contact

The method allows you to make changes to an existing contact: change the phone number, data in the contact’s custom fields, and add the contact to the list.

**Please note:** that in the TEST account mode there is a restriction for performing this method: you can only change the contact’s phone number to a verified number (number verification is performed in the personal account at the platform)

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_update200_response import ContactUpdate200Response
from bsg_api.models.contact_update_request import ContactUpdateRequest
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
    api_instance = bsg_api.ContactUpdateApi(api_client)
    id = 56 # int | Contact id
    contact_update_request = {"phone":61401629754,"fields":[{"id":387714,"value":"Ilya Muromets"}],"groups":[1864618]} # ContactUpdateRequest | 

    try:
        # Update contact
        api_response = api_instance.contact_update(id, contact_update_request)
        print("The response of ContactUpdateApi->contact_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactUpdateApi->contact_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact id |  |
| **contact_update_request** | [**ContactUpdateRequest**](ContactUpdateRequest.md) |  |  |

### Return type

[**ContactUpdate200Response**](ContactUpdate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful updated |  -  |
| **422** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

