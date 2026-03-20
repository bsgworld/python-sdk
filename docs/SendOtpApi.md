# bsg_api.SendOtpApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**send_otp**](SendOtpApi.md#send_otp) | **POST** /api/2fa/authentications/otp | Send One-time password |


# **send_otp**
> SendOtp201Response send_otp(send_otp_request)

Send One-time password

This API call is used to generate and send a one-time password to a user in an SMS or Viber message. **Please note:** authentication of recipients who are in the SMS or Viber stop list in your contact book is not possible using the corresponding method. (That is, if the recipient is in the SMS stop list, then when requesting authentication using the SMS method, the one-time password will not be sent, and you will receive an error in response).

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.send_otp201_response import SendOtp201Response
from bsg_api.models.send_otp_request import SendOtpRequest
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
    api_instance = bsg_api.SendOtpApi(api_client)
    send_otp_request = {"recipient":"61401629754","channel":"sms","sender":"SENDER","template_id":"12","code_lifetime":300,"code_max_tries":3,"code_digits":5} # SendOtpRequest | 

    try:
        # Send One-time password
        api_response = api_instance.send_otp(send_otp_request)
        print("The response of SendOtpApi->send_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SendOtpApi->send_otp: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_otp_request** | [**SendOtpRequest**](SendOtpRequest.md) |  |  |

### Return type

[**SendOtp201Response**](SendOtp201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful operation: TwoFA OTP generation &amp; authentication session |  -  |
| **422** | The given data was invalid. |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

