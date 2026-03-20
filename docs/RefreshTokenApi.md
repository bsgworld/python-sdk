# bsg_api.RefreshTokenApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**refresh_token**](RefreshTokenApi.md#refresh_token) | **POST** /api/auth/refresh | Refresh JWT token |


# **refresh_token**
> TokenSchema refresh_token()

Refresh JWT token

Refresh JWT token. Return new JWT-token to new term. It's necessary to call when actual JWT-token almost expired

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.token_schema import TokenSchema
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
    api_instance = bsg_api.RefreshTokenApi(api_client)

    try:
        # Refresh JWT token
        api_response = api_instance.refresh_token()
        print("The response of RefreshTokenApi->refresh_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RefreshTokenApi->refresh_token: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**TokenSchema**](TokenSchema.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

