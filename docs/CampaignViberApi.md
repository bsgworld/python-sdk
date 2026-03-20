# bsg_api.CampaignViberApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**viber_send**](CampaignViberApi.md#viber_send) | **POST** /api/campaigns/viber/send | Send Viber campaign |


# **viber_send**
> ViberCampaignResponse viber_send(send_viber_campaign)

Send Viber campaign

This method provides the ability to send a viber campaign.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.send_viber_campaign import SendViberCampaign
from bsg_api.models.viber_campaign_response import ViberCampaignResponse
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
    api_instance = bsg_api.CampaignViberApi(api_client)
    send_viber_campaign = {"phones":[{"number":"380971123456"}],"text":"some viber text","sender":"Notify"} # SendViberCampaign | 

    try:
        # Send Viber campaign
        api_response = api_instance.viber_send(send_viber_campaign)
        print("The response of CampaignViberApi->viber_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignViberApi->viber_send: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **send_viber_campaign** | [**SendViberCampaign**](SendViberCampaign.md) |  |  |

### Return type

[**ViberCampaignResponse**](ViberCampaignResponse.md)

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

