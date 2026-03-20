# bsg_api.LoginApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**login**](LoginApi.md#login) | **POST** /api/auth/login | Receive JWT token |


# **login**
> TokenSchema login(login_request)

Receive JWT token

Receive JWT token to use with other method. Use live/test api-key to login. JWT-token has limited lifetime and have to be refreshed before become expired

### Example


```python
import bsg_api
from bsg_api.models.login_request import LoginRequest
from bsg_api.models.token_schema import TokenSchema
from bsg_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://one-api.bsg.world
# See configuration.py for a list of all supported configuration parameters.
configuration = bsg_api.Configuration(
    host = "https://one-api.bsg.world"
)


# Enter a context with an instance of the API client
with bsg_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = bsg_api.LoginApi(api_client)
    login_request = {"api_key":"live_XXXXXXXXXXXXXXXXXXXX"} # LoginRequest | 

    try:
        # Receive JWT token
        api_response = api_instance.login(login_request)
        print("The response of LoginApi->login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LoginApi->login: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **login_request** | [**LoginRequest**](LoginRequest.md) |  |  |

### Return type

[**TokenSchema**](TokenSchema.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

