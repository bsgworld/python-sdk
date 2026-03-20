# bsg_api.CancelOtpApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_otp**](CancelOtpApi.md#cancel_otp) | **POST** /api/2fa/authentications/{id}/cancel | Cancel the authentication session |


# **cancel_otp**
> CancelOtp200Response cancel_otp(id)

Cancel the authentication session

Used to cancel the authentication process. In this case, authentication must be in the Pending status.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.cancel_otp200_response import CancelOtp200Response
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
    api_instance = bsg_api.CancelOtpApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

    try:
        # Cancel the authentication session
        api_response = api_instance.cancel_otp(id)
        print("The response of CancelOtpApi->cancel_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CancelOtpApi->cancel_otp: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. |  |

### Return type

[**CancelOtp200Response**](CancelOtp200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA OTP cancellation |  -  |
| **404** | Authentication not found |  -  |
| **422** | Authentication failed status |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

