# bsg_api.TwoFAOTPApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_otp**](TwoFAOTPApi.md#cancel_otp) | **POST** /api/2fa/authentications/{id}/cancel | Cancel the authentication session |
| [**otp_list**](TwoFAOTPApi.md#otp_list) | **GET** /api/2fa/authentications | List of authentication sessions |
| [**resend_otp**](TwoFAOTPApi.md#resend_otp) | **POST** /api/2fa/authentications/otp/{id}/resend | Resend the one-time code |
| [**send_otp**](TwoFAOTPApi.md#send_otp) | **POST** /api/2fa/authentications/otp | Send One-time password |
| [**status_otp**](TwoFAOTPApi.md#status_otp) | **GET** /api/2fa/authentications/{id} | Check authentication status |
| [**verify_otp**](TwoFAOTPApi.md#verify_otp) | **POST** /api/2fa/authentications/otp/{id}/verify | Check one-time Code |


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
    api_instance = bsg_api.TwoFAOTPApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

    try:
        # Cancel the authentication session
        api_response = api_instance.cancel_otp(id)
        print("The response of TwoFAOTPApi->cancel_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TwoFAOTPApi->cancel_otp: %s\n" % e)
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

# **otp_list**
> OtpList200Response otp_list(filter_from, filter_to, page_offset=page_offset, page_limit=page_limit, filter_ids=filter_ids, filter_status=filter_status, filter_channel=filter_channel, filter_recipient=filter_recipient, filter_country_code=filter_country_code, way=way, sort=sort)

List of authentication sessions

Use to get a list of authentications for a period.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.otp_channel import OtpChannel
from bsg_api.models.otp_list200_response import OtpList200Response
from bsg_api.models.otp_status import OtpStatus
from bsg_api.models.sort_way import SortWay
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
    api_instance = bsg_api.TwoFAOTPApi(api_client)
    filter_from = 'Thu Dec 01 00:00:00 UTC 2022' # date | Period start date (date and time when the authentication session was created) in ISO 8601 format.
    filter_to = 'Sat Dec 31 00:00:00 UTC 2022' # date | End date of the period (date and time when the authentication was created) in ISO 8601 format.
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 10 # int |  (optional) (default to 10)
    filter_ids = ['filter_ids_example'] # List[str] | Authentication ID. The maximum number is 3. (optional)
    filter_status = bsg_api.OtpStatus() # OtpStatus |  (optional)
    filter_channel = bsg_api.OtpChannel() # OtpChannel |  (optional)
    filter_recipient = 'filter_recipient_example' # str |  (optional)
    filter_country_code = 'filter_country_code_example' # str |  (optional)
    way = asc # SortWay |  (optional) (default to asc)
    sort = id # str | Sort by (optional) (default to id)

    try:
        # List of authentication sessions
        api_response = api_instance.otp_list(filter_from, filter_to, page_offset=page_offset, page_limit=page_limit, filter_ids=filter_ids, filter_status=filter_status, filter_channel=filter_channel, filter_recipient=filter_recipient, filter_country_code=filter_country_code, way=way, sort=sort)
        print("The response of TwoFAOTPApi->otp_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TwoFAOTPApi->otp_list: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filter_from** | **date** | Period start date (date and time when the authentication session was created) in ISO 8601 format. |  |
| **filter_to** | **date** | End date of the period (date and time when the authentication was created) in ISO 8601 format. |  |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** |  | [optional] [default to 10] |
| **filter_ids** | [**List[str]**](str.md) | Authentication ID. The maximum number is 3. | [optional]  |
| **filter_status** | [**OtpStatus**](.md) |  | [optional]  |
| **filter_channel** | [**OtpChannel**](.md) |  | [optional]  |
| **filter_recipient** | **str** |  | [optional]  |
| **filter_country_code** | **str** |  | [optional]  |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **sort** | **str** | Sort by | [optional] [default to id] |

### Return type

[**OtpList200Response**](OtpList200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA authentications list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = bsg_api.TwoFAOTPApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

    try:
        # Resend the one-time code
        api_response = api_instance.resend_otp(id)
        print("The response of TwoFAOTPApi->resend_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TwoFAOTPApi->resend_otp: %s\n" % e)
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
    api_instance = bsg_api.TwoFAOTPApi(api_client)
    send_otp_request = {"recipient":"61401629754","channel":"sms","sender":"SENDER","template_id":"12","code_lifetime":300,"code_max_tries":3,"code_digits":5} # SendOtpRequest | 

    try:
        # Send One-time password
        api_response = api_instance.send_otp(send_otp_request)
        print("The response of TwoFAOTPApi->send_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TwoFAOTPApi->send_otp: %s\n" % e)
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
    api_instance = bsg_api.TwoFAOTPApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

    try:
        # Check authentication status
        api_response = api_instance.status_otp(id)
        print("The response of TwoFAOTPApi->status_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TwoFAOTPApi->status_otp: %s\n" % e)
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
    api_instance = bsg_api.TwoFAOTPApi(api_client)
    id = 'ea5db413-e368-4952-b745-cc2030210c49' # str | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.
    verify_otp_request = bsg_api.VerifyOtpRequest() # VerifyOtpRequest | 

    try:
        # Check one-time Code
        api_response = api_instance.verify_otp(id, verify_otp_request)
        print("The response of TwoFAOTPApi->verify_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TwoFAOTPApi->verify_otp: %s\n" % e)
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

