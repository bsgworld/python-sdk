# bsg_api.CampaignWhatsAppApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**post_campaigns_whatsapp_send**](CampaignWhatsAppApi.md#post_campaigns_whatsapp_send) | **POST** /api/campaigns/whatsapp/send | Send WhatsApp campaign |


# **post_campaigns_whatsapp_send**
> CampaignSchema post_campaigns_whatsapp_send(send_whats_app_campaign)

Send WhatsApp campaign

This method allows you to send a whatsapp. The same message will be sent to list of phones

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.campaign_schema import CampaignSchema
from bsg_api.models.send_whats_app_campaign import SendWhatsAppCampaign
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
    api_instance = bsg_api.CampaignWhatsAppApi(api_client)
    send_whats_app_campaign = bsg_api.SendWhatsAppCampaign() # SendWhatsAppCampaign | 

    try:
        # Send WhatsApp campaign
        api_response = api_instance.post_campaigns_whatsapp_send(send_whats_app_campaign)
        print("The response of CampaignWhatsAppApi->post_campaigns_whatsapp_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignWhatsAppApi->post_campaigns_whatsapp_send: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_whats_app_campaign** | [**SendWhatsAppCampaign**](SendWhatsAppCampaign.md) |  |  |

### Return type

[**CampaignSchema**](CampaignSchema.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Campaign info |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

