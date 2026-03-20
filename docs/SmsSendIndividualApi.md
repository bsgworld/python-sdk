# bsg_api.SmsSendIndividualApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**sms_send_individual**](SmsSendIndividualApi.md#sms_send_individual) | **POST** /api/campaigns/sms/send-individual | Send SMS with different text |


# **sms_send_individual**
> SmsCampaignResponse sms_send_individual(sms_send_individual_request)

Send SMS with different text

Send SMS with different text to list of phones

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.sms_campaign_response import SmsCampaignResponse
from bsg_api.models.sms_send_individual_request import SmsSendIndividualRequest
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
    api_instance = bsg_api.SmsSendIndividualApi(api_client)
    sms_send_individual_request = {"messages":[{"phone":380661231231,"text":"hello Jack","sender":"Vet klinika"},{"phone":380661231232,"text":"hello Anna","sender":"Vet klinika"},{"phone":380661231233,"text":"Hi Hellen","sender":"Vet klinika"}]} # SmsSendIndividualRequest | 

    try:
        # Send SMS with different text
        api_response = api_instance.sms_send_individual(sms_send_individual_request)
        print("The response of SmsSendIndividualApi->sms_send_individual:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SmsSendIndividualApi->sms_send_individual: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sms_send_individual_request** | [**SmsSendIndividualRequest**](SmsSendIndividualRequest.md) |  |  |

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

