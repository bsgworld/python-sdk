# bsg_api.OtpTemplateDeleteApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**otp_template_delete**](OtpTemplateDeleteApi.md#otp_template_delete) | **DELETE** /api/2fa/authentications/templates/{templateId} | Delete a message template |


# **otp_template_delete**
> OtpTemplateDelete200Response otp_template_delete(template_id)

Delete a message template

This method deletes the message template for sending the OTP code based on its unique identifier.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.otp_template_delete200_response import OtpTemplateDelete200Response
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
    api_instance = bsg_api.OtpTemplateDeleteApi(api_client)
    template_id = 56 # int | The ID of the message template that you want to delete. From 1 to 9 digits.

    try:
        # Delete a message template
        api_response = api_instance.otp_template_delete(template_id)
        print("The response of OtpTemplateDeleteApi->otp_template_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OtpTemplateDeleteApi->otp_template_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **int** | The ID of the message template that you want to delete. From 1 to 9 digits. |  |

### Return type

[**OtpTemplateDelete200Response**](OtpTemplateDelete200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |
| **422** | Default template is not available for deletion |  -  |
| **404** | Template not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

