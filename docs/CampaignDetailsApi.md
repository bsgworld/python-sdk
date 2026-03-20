# bsg_api.CampaignDetailsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**campaign_details**](CampaignDetailsApi.md#campaign_details) | **GET** /api/campaigns/{id}/detail | Get campaign details |


# **campaign_details**
> CampaignDetails200Response campaign_details(id)

Get campaign details

Campaign detail information and delivery statistics

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.campaign_details200_response import CampaignDetails200Response
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
    api_instance = bsg_api.CampaignDetailsApi(api_client)
    id = 53651994 # int | 

    try:
        # Get campaign details
        api_response = api_instance.campaign_details(id)
        print("The response of CampaignDetailsApi->campaign_details:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignDetailsApi->campaign_details: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |

### Return type

[**CampaignDetails200Response**](CampaignDetails200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Campaign details |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

