# bsg_api.SmsSendApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**sms_send**](SmsSendApi.md#sms_send) | **POST** /api/campaigns/sms/send | Send SMS campaign |


# **sms_send**
> SmsCampaignResponse sms_send(sms_send_request)

Send SMS campaign

The method allows sending an SMS. The same text to list of phones will sent as single campaign

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.sms_campaign_response import SmsCampaignResponse
from bsg_api.models.sms_send_request import SmsSendRequest
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
    api_instance = bsg_api.SmsSendApi(api_client)
    sms_send_request = {"phones":[{"number":380661231231}],"sender":"Vet klinika","text":"test"} # SmsSendRequest | 

    try:
        # Send SMS campaign
        api_response = api_instance.sms_send(sms_send_request)
        print("The response of SmsSendApi->sms_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SmsSendApi->sms_send: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sms_send_request** | [**SmsSendRequest**](SmsSendRequest.md) |  |  |

### Return type

[**SmsCampaignResponse**](SmsCampaignResponse.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Campaign info |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

