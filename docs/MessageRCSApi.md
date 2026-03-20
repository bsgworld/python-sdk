# bsg_api.MessageRCSApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**rcs_single**](MessageRCSApi.md#rcs_single) | **POST** /api/messages/rcs/send | Send single RCS message |


# **rcs_single**
> MessageResponse rcs_single(rcs_message)

Send single RCS message

This method allows you to send a single rcs message instantly. The message is sent without creating a campaign, provided that the client has enough funds on his/her balance. The ability to send messages via an alternative SMS channel is also supported

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.message_response import MessageResponse
from bsg_api.models.rcs_message import RcsMessage
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
    api_instance = bsg_api.MessageRCSApi(api_client)
    rcs_message = {"phone":{"number":"380661231231"},"sender":"rcs_sender","options":{"text":"Hello! ☺️"}} # RcsMessage | 

    try:
        # Send single RCS message
        api_response = api_instance.rcs_single(rcs_message)
        print("The response of MessageRCSApi->rcs_single:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MessageRCSApi->rcs_single: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rcs_message** | [**RcsMessage**](RcsMessage.md) |  |  |

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

