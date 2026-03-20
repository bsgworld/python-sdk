# bsg_api.VerifyOtpApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**verify_otp**](VerifyOtpApi.md#verify_otp) | **POST** /api/2fa/authentications/otp/{id}/verify | Check one-time Code |


# **verify_otp**
> VerifyOtp200Response verify_otp(id, verify_otp_request)

Check one-time Code

The API call is used to verify that the one-time password you received from the user matches the one sent by BSG

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.verify_otp200_response import VerifyOtp200Response
from bsg_api.models.verify_otp_request import VerifyOtpRequest
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
    api_instance = bsg_api.VerifyOtpApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.
    verify_otp_request = bsg_api.VerifyOtpRequest() # VerifyOtpRequest | 

    try:
        # Check one-time Code
        api_response = api_instance.verify_otp(id, verify_otp_request)
        print("The response of VerifyOtpApi->verify_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VerifyOtpApi->verify_otp: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. |  |
| **verify_otp_request** | [**VerifyOtpRequest**](VerifyOtpRequest.md) |  |  |

### Return type

[**VerifyOtp200Response**](VerifyOtp200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA OTP verifying |  -  |
| **404** | Wrong code or authentication not found |  -  |
| **422** | Authentication failed status |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

