# bsg_api.OtpTemplateCreateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**otp_template_create**](OtpTemplateCreateApi.md#otp_template_create) | **POST** /api/2fa/authentications/templates | Create a message template |


# **otp_template_create**
> OtpTemplateCreate200Response otp_template_create(otp_template_create_request)

Create a message template

This method creates a new message template used for sending the OTP code.  

**Please note** *that after creating the template, it is moderated. This template will be available for sending messages
with the OTP code only after moderation. Once it’s ready, its status will be changed from Requested to Approved.*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.otp_template_create200_response import OtpTemplateCreate200Response
from bsg_api.models.otp_template_create_request import OtpTemplateCreateRequest
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
    api_instance = bsg_api.OtpTemplateCreateApi(api_client)
    otp_template_create_request = bsg_api.OtpTemplateCreateRequest() # OtpTemplateCreateRequest | 

    try:
        # Create a message template
        api_response = api_instance.otp_template_create(otp_template_create_request)
        print("The response of OtpTemplateCreateApi->otp_template_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OtpTemplateCreateApi->otp_template_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **otp_template_create_request** | [**OtpTemplateCreateRequest**](OtpTemplateCreateRequest.md) |  |  |

### Return type

[**OtpTemplateCreate200Response**](OtpTemplateCreate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Stored template info |  -  |
| **422** | The given data was invalid. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

