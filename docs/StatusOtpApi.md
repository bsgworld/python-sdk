# bsg_api.StatusOtpApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**status_otp**](StatusOtpApi.md#status_otp) | **GET** /api/2fa/authentications/{id} | Check authentication status |


# **status_otp**
> StatusOtp200Response status_otp(id)

Check authentication status

Use to get information about the current authentication status by specifying its identifier.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.status_otp200_response import StatusOtp200Response
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
    api_instance = bsg_api.StatusOtpApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

    try:
        # Check authentication status
        api_response = api_instance.status_otp(id)
        print("The response of StatusOtpApi->status_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatusOtpApi->status_otp: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. |  |

### Return type

[**StatusOtp200Response**](StatusOtp200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA OTP getting an info |  -  |
| **404** | Authentication not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

