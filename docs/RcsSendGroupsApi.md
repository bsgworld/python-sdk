# bsg_api.RcsSendGroupsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**rcs_send**](RcsSendGroupsApi.md#rcs_send) | **POST** /api/campaigns/rcs/send | Send RCS message |


# **rcs_send**
> RcsSend200Response rcs_send(send_rcs_campaign)

Send RCS message

This method provides the ability to send a single rcs message or to send a mass rcs message.
It also supports sending messages via an alternative SMS channel if the rcs can’t be delivered

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.rcs_send200_response import RcsSend200Response
from bsg_api.models.send_rcs_campaign import SendRcsCampaign
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
    api_instance = bsg_api.RcsSendGroupsApi(api_client)
    send_rcs_campaign = {"phones":[{"number":"380661231231"}],"sender":"rcs_sender","options":{"text":"Hello! ☺️"}} # SendRcsCampaign | 

    try:
        # Send RCS message
        api_response = api_instance.rcs_send(send_rcs_campaign)
        print("The response of RcsSendGroupsApi->rcs_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RcsSendGroupsApi->rcs_send: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_rcs_campaign** | [**SendRcsCampaign**](SendRcsCampaign.md) |  |  |

### Return type

[**RcsSend200Response**](RcsSend200Response.md)

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

