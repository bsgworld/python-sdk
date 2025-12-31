# bsg_api.AccountSettingsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_settings_address_book_fields_by_id**](AccountSettingsApi.md#get_settings_address_book_fields_by_id) | **GET** /api/settings/address-book-fields/{id} | Get settings value |


# **get_settings_address_book_fields_by_id**
> object get_settings_address_book_fields_by_id(id)

Get settings value

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
    api_instance = bsg_api.AccountSettingsApi(api_client)
    id = 1 # int | Address Book ID

    try:
        # Get settings value
        api_response = api_instance.get_settings_address_book_fields_by_id(id)
        print("The response of AccountSettingsApi->get_settings_address_book_fields_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountSettingsApi->get_settings_address_book_fields_by_id: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Address Book ID |  |

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
| **200** | Atompark address book fields |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

