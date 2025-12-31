# bsg_api.BalanceApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**account_balance**](BalanceApi.md#account_balance) | **GET** /api/accounts/balance | Get balance |
| [**account_tariffs**](BalanceApi.md#account_tariffs) | **GET** /api/accounts/tariff | Get tariffs |


# **account_balance**
> AccountBalance200Response account_balance()

Get balance

Platform provides an API to get information about your account balance.
The request allows you to obtain information about the current balance of your account, including the credit limit

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.account_balance200_response import AccountBalance200Response
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
    api_instance = bsg_api.BalanceApi(api_client)

    try:
        # Get balance
        api_response = api_instance.account_balance()
        print("The response of BalanceApi->account_balance:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BalanceApi->account_balance: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountBalance200Response**](AccountBalance200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Account balance data |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **account_tariffs**
> AccountTariffs200Response account_tariffs(page_offset=page_offset, page_limit=page_limit)

Get tariffs

This API allows you to get detailed information about the tariffs for sending SMS and Viber messages, as well as phone Number Verifier requests.

All rates are specified in the currency that is set in the account settings on the Platform.

The method transmits information about all available account tariffs for the SMS / 2 Way SMS, Viber, and Number Verifier service

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.account_tariffs200_response import AccountTariffs200Response
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
    api_instance = bsg_api.BalanceApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)

    try:
        # Get tariffs
        api_response = api_instance.account_tariffs(page_offset=page_offset, page_limit=page_limit)
        print("The response of BalanceApi->account_tariffs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BalanceApi->account_tariffs: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |

### Return type

[**AccountTariffs200Response**](AccountTariffs200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | List of the tariffs |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

