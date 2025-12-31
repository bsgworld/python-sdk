# bsg_api.InternalWstPriceApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_internal_wst_prices**](InternalWstPriceApi.md#get_internal_wst_prices) | **GET** /api/internal/wst/prices | Get price list for each country |
| [**get_internal_wst_prices_by_country_code**](InternalWstPriceApi.md#get_internal_wst_prices_by_country_code) | **GET** /api/internal/wst/prices/{countryCode} | Get prices for country |


# **get_internal_wst_prices**
> GetInternalWstPrices200Response get_internal_wst_prices(product)

Get price list for each country

### Example

* Bearer (JWT) Authentication (InternalAuth):

```python
import bsg_api
from bsg_api.models.get_internal_wst_prices200_response import GetInternalWstPrices200Response
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
    api_instance = bsg_api.InternalWstPriceApi(api_client)
    product = 'product_example' # str | Product value

    try:
        # Get price list for each country
        api_response = api_instance.get_internal_wst_prices(product)
        print("The response of InternalWstPriceApi->get_internal_wst_prices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InternalWstPriceApi->get_internal_wst_prices: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product** | **str** | Product value |  |

### Return type

[**GetInternalWstPrices200Response**](GetInternalWstPrices200Response.md)

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

# **get_internal_wst_prices_by_country_code**
> GetInternalWstPricesByCountryCode200Response get_internal_wst_prices_by_country_code(country_code, product)

Get prices for country

### Example

* Bearer (JWT) Authentication (InternalAuth):

```python
import bsg_api
from bsg_api.models.get_internal_wst_prices_by_country_code200_response import GetInternalWstPricesByCountryCode200Response
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
    api_instance = bsg_api.InternalWstPriceApi(api_client)
    country_code = 'AB' # str | Country ISO Code
    product = 'product_example' # str | Product value

    try:
        # Get prices for country
        api_response = api_instance.get_internal_wst_prices_by_country_code(country_code, product)
        print("The response of InternalWstPriceApi->get_internal_wst_prices_by_country_code:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InternalWstPriceApi->get_internal_wst_prices_by_country_code: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **str** | Country ISO Code |  |
| **product** | **str** | Product value |  |

### Return type

[**GetInternalWstPricesByCountryCode200Response**](GetInternalWstPricesByCountryCode200Response.md)

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

