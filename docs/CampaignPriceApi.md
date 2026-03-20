# bsg_api.CampaignPriceApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**campaign_price**](CampaignPriceApi.md#campaign_price) | **POST** /api/campaigns/price | Calculate campaign price |


# **campaign_price**
> CampaignPrice200Response campaign_price(campaign_price_request)

Calculate campaign price

Calculate campaign estimated price before actually [send it](#operation/sms_send)

**Please note:** Method suitable only for SMS campaigns


### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.campaign_price200_response import CampaignPrice200Response
from bsg_api.models.campaign_price_request import CampaignPriceRequest
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
    api_instance = bsg_api.CampaignPriceApi(api_client)
    campaign_price_request = {"sender":"Vet klinika","text":"hello!","messages":[{"phone":38267161234}]} # CampaignPriceRequest | 

    try:
        # Calculate campaign price
        api_response = api_instance.campaign_price(campaign_price_request)
        print("The response of CampaignPriceApi->campaign_price:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignPriceApi->campaign_price: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **campaign_price_request** | [**CampaignPriceRequest**](CampaignPriceRequest.md) |  |  |

### Return type

[**CampaignPrice200Response**](CampaignPrice200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Campaign price |  -  |
| **422** | Error |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

