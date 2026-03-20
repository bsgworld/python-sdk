# bsg_api.AccountBalanceApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**account_balance**](AccountBalanceApi.md#account_balance) | **GET** /api/accounts/balance | Get balance |


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
    api_instance = bsg_api.AccountBalanceApi(api_client)

    try:
        # Get balance
        api_response = api_instance.account_balance()
        print("The response of AccountBalanceApi->account_balance:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountBalanceApi->account_balance: %s\n" % e)
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

