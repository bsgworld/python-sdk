# bsg_api.MessagesWhatsAppApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**whatsapp_single**](MessagesWhatsAppApi.md#whatsapp_single) | **POST** /api/messages/whatsapp/send | Send single WhatsApp message |


# **whatsapp_single**
> WhatsappSingle200Response whatsapp_single(whats_app_message)

Send single WhatsApp message

This method allows you to send a single whatsapp message instantly. The message is sent without creating a campaign, provided that the client has enough funds on his/her balance. The ability to send messages via an alternative SMS channel is also supported

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.whats_app_message import WhatsAppMessage
from bsg_api.models.whatsapp_single200_response import WhatsappSingle200Response
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
    api_instance = bsg_api.MessagesWhatsAppApi(api_client)
    whats_app_message = {"phone":{"number":"380661231231"},"sender":"whatsapp_sender","template":{"name":"whatsapp_test","language":{"code":"en"},"components":[{"type":"body","parameters":[{"type":"text","text":"Hello! ☺️"}]}]}} # WhatsAppMessage | 

    try:
        # Send single WhatsApp message
        api_response = api_instance.whatsapp_single(whats_app_message)
        print("The response of MessagesWhatsAppApi->whatsapp_single:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MessagesWhatsAppApi->whatsapp_single: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **whats_app_message** | [**WhatsAppMessage**](WhatsAppMessage.md) |  |  |

### Return type

[**WhatsappSingle200Response**](WhatsappSingle200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Message info |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

