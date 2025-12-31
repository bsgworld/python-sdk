# bsg_api.InternalTwoFAApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_internal2fa_authentications_full_price**](InternalTwoFAApi.md#get_internal2fa_authentications_full_price) | **GET** /api/internal/2fa/authentications/full-price | Show TwoFA authentication full price |


# **get_internal2fa_authentications_full_price**
> GetInternal2faAuthenticationsFullPrice200Response get_internal2fa_authentications_full_price(channel_type, currency, tariff_code=tariff_code, country_code=country_code, operator_id=operator_id)

Show TwoFA authentication full price

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.get_internal2fa_authentications_full_price200_response import GetInternal2faAuthenticationsFullPrice200Response
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
    api_instance = bsg_api.InternalTwoFAApi(api_client)
    channel_type = 'channel_type_example' # str | 
    currency = 'EUR' # str | 
    tariff_code = 28 # int |  (optional)
    country_code = 'UA' # str |  (optional)
    operator_id = 1 # int |  (optional)

    try:
        # Show TwoFA authentication full price
        api_response = api_instance.get_internal2fa_authentications_full_price(channel_type, currency, tariff_code=tariff_code, country_code=country_code, operator_id=operator_id)
        print("The response of InternalTwoFAApi->get_internal2fa_authentications_full_price:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InternalTwoFAApi->get_internal2fa_authentications_full_price: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channel_type** | **str** |  |  |
| **currency** | **str** |  |  |
| **tariff_code** | **int** |  | [optional]  |
| **country_code** | **str** |  | [optional]  |
| **operator_id** | **int** |  | [optional]  |

### Return type

[**GetInternal2faAuthenticationsFullPrice200Response**](GetInternal2faAuthenticationsFullPrice200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA OTP getting an info |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

