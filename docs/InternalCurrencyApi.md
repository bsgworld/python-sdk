# bsg_api.InternalCurrencyApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_internal_currencies**](InternalCurrencyApi.md#get_internal_currencies) | **GET** /api/internal/currencies | Get currencies list  |


# **get_internal_currencies**
> GetInternalCurrencies200Response get_internal_currencies(currency_code=currency_code)

Get currencies list 

### Example

* Bearer (JWT) Authentication (InternalAuth):

```python
import bsg_api
from bsg_api.models.get_internal_currencies200_response import GetInternalCurrencies200Response
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

# Configure Bearer authorization (JWT): InternalAuth
configuration = bsg_api.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with bsg_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = bsg_api.InternalCurrencyApi(api_client)
    currency_code = 'USD' # str | Product value (optional)

    try:
        # Get currencies list 
        api_response = api_instance.get_internal_currencies(currency_code=currency_code)
        print("The response of InternalCurrencyApi->get_internal_currencies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InternalCurrencyApi->get_internal_currencies: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency_code** | **str** | Product value | [optional]  |

### Return type

[**GetInternalCurrencies200Response**](GetInternalCurrencies200Response.md)

### Authorization

[InternalAuth](../README.md#InternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

