# bsg_api.MessagesApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**send_message**](MessagesApi.md#send_message) | **POST** /api/messages/send | Send single message |


# **send_message**
> MessageResponse send_message(message_universal)

Send single message

This method allows you to send a single message of any type instantly. The message may be one of: sms, rcs, whatsapp. The message is sent without creating a campaign, provided that the client has enough funds on his/her balance. The ability to send messages via an alternative SMS channel is also supported

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.message_response import MessageResponse
from bsg_api.models.message_universal import MessageUniversal
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
    api_instance = bsg_api.MessagesApi(api_client)
    message_universal = {"channels":["sms"],"phone":{"number":"380661231231"},"sms":{"sender":"test","text":"Hello!"}} # MessageUniversal | 

    try:
        # Send single message
        api_response = api_instance.send_message(message_universal)
        print("The response of MessagesApi->send_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MessagesApi->send_message: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message_universal** | [**MessageUniversal**](MessageUniversal.md) |  |  |

### Return type

[**MessageResponse**](MessageResponse.md)

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

