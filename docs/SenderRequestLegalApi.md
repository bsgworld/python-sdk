# bsg_api.SenderRequestLegalApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**sender_request_legal**](SenderRequestLegalApi.md#sender_request_legal) | **POST** /api/senders/requests/legal | Sender registration by a legal entity |


# **sender_request_legal**
> SenderRequestLegal201Response sender_request_legal(sender_request_legal_request)

Sender registration by a legal entity

Method for submitting an application for registration of the SMS Sender’s name (Alpha-name) with a mobile operator by a subject legal entity.

**Please note:** that Sender registration is not available in Demo and Test account modes.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.sender_request_legal201_response import SenderRequestLegal201Response
from bsg_api.models.sender_request_legal_request import SenderRequestLegalRequest
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
    api_instance = bsg_api.SenderRequestLegalApi(api_client)
    sender_request_legal_request = bsg_api.SenderRequestLegalRequest() # SenderRequestLegalRequest | 

    try:
        # Sender registration by a legal entity
        api_response = api_instance.sender_request_legal(sender_request_legal_request)
        print("The response of SenderRequestLegalApi->sender_request_legal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SenderRequestLegalApi->sender_request_legal: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sender_request_legal_request** | [**SenderRequestLegalRequest**](SenderRequestLegalRequest.md) |  |  |

### Return type

[**SenderRequestLegal201Response**](SenderRequestLegal201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

