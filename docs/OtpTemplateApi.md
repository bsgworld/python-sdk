# bsg_api.OtpTemplateApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**otp_template**](OtpTemplateApi.md#otp_template) | **GET** /api/2fa/authentications/templates/{templateId} | Get message template |


# **otp_template**
> OtpTemplate200Response otp_template(template_id)

Get message template

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.otp_template200_response import OtpTemplate200Response
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
    api_instance = bsg_api.OtpTemplateApi(api_client)
    template_id = 56 # int | Template id

    try:
        # Get message template
        api_response = api_instance.otp_template(template_id)
        print("The response of OtpTemplateApi->otp_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OtpTemplateApi->otp_template: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **int** | Template id |  |

### Return type

[**OtpTemplate200Response**](OtpTemplate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Get template info |  -  |
| **404** | Model not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

