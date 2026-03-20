# bsg_api.ResendOtpApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**resend_otp**](ResendOtpApi.md#resend_otp) | **POST** /api/2fa/authentications/otp/{id}/resend | Resend the one-time code |


# **resend_otp**
> ResendOtp200Response resend_otp(id)

Resend the one-time code

sed to resend the one-time password to the recipient: a new one-time password is generated and
sent in the message, and the previous one becomes invalid. When resending, already saved data is used to generate the
OTP from the request [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp).

*This API call is available only if the current authentication is not completed before its expiration date
(the authentication validity period is specified in each TwoFA API response).*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.resend_otp200_response import ResendOtp200Response
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
    api_instance = bsg_api.ResendOtpApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

    try:
        # Resend the one-time code
        api_response = api_instance.resend_otp(id)
        print("The response of ResendOtpApi->resend_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResendOtpApi->resend_otp: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. |  |

### Return type

[**ResendOtp200Response**](ResendOtp200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA OTP resending |  -  |
| **404** | Authentication not found |  -  |
| **422** | Authentication failed status |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

