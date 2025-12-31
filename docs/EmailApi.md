# bsg_api.EmailApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**email_send**](EmailApi.md#email_send) | **POST** /api/email/send-emails | Send Email |
| [**email_template_send**](EmailApi.md#email_template_send) | **POST** /api/email/send-template-emails | Send Email template |


# **email_send**
> EmailResponse email_send(send_email)

Send Email

Method is designed for sending single email with optional parameters.  

This request allows you to send emails with both text and HTML content, and optionally include inline media, such as images or other files, which are embedded directly in the email body for a richer user experience

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.email_response import EmailResponse
from bsg_api.models.send_email import SendEmail
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
    api_instance = bsg_api.EmailApi(api_client)
    send_email = {"to":["user@test.com"],"from":"Test.email 11_22 <user@test1.email.bsg.world>","subject":"test1","htmlbody":"<html><head><title>link to Symbl.cc</title></head><body><h1>Visit site</h1>Visit site <a href=\"https://symbl.cc\">Symbl.cc</a> for additional information.</body></html>"} # SendEmail | 

    try:
        # Send Email
        api_response = api_instance.email_send(send_email)
        print("The response of EmailApi->email_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->email_send: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_email** | [**SendEmail**](SendEmail.md) |  |  |

### Return type

[**EmailResponse**](EmailResponse.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Message received |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **email_template_send**
> EmailResponse email_template_send(send_template_email)

Send Email template

Method allows you to send an email with dynamic content by referencing an email template (specifying template id).
You can customize the content of the email with variables, and you also have the option to embed inline media files

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.email_response import EmailResponse
from bsg_api.models.send_template_email import SendTemplateEmail
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
    api_instance = bsg_api.EmailApi(api_client)
    send_template_email = {"to":["user@test.com"],"from":"Test.email 11_22 <user@test1.email.bsg.world>","subject":"test1","template_id":19,"template_content":{"recipients_name":"Test User","company_name":"Company Name"}} # SendTemplateEmail | 

    try:
        # Send Email template
        api_response = api_instance.email_template_send(send_template_email)
        print("The response of EmailApi->email_template_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->email_template_send: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_template_email** | [**SendTemplateEmail**](SendTemplateEmail.md) |  |  |

### Return type

[**EmailResponse**](EmailResponse.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Message received |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

