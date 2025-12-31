# bsg_api.CampaignSMSApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**sms_send**](CampaignSMSApi.md#sms_send) | **POST** /api/campaigns/sms/send | Send SMS campaign |
| [**sms_send_groups**](CampaignSMSApi.md#sms_send_groups) | **POST** /api/campaigns/sms/send-groups | Send SMS to contact list |
| [**sms_send_individual**](CampaignSMSApi.md#sms_send_individual) | **POST** /api/campaigns/sms/send-individual | Send SMS with different text |


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
    api_instance = bsg_api.CampaignSMSApi(api_client)
    sms_send_request = {"phones":[{"number":380661231231}],"sender":"Vet klinika","text":"test"} # SmsSendRequest | 

    try:
        # Send SMS campaign
        api_response = api_instance.sms_send(sms_send_request)
        print("The response of CampaignSMSApi->sms_send:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignSMSApi->sms_send: %s\n" % e)
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

# **sms_send_groups**
> SmsCampaignResponse sms_send_groups(sms_send_groups_request)

Send SMS to contact list

The method allows sending an SMS to the contacts list from the Contact Book. The campaign can contain personalized data from the contact fields in the text of the message for each contact. 

It is possible to specify no more than 10 000 contacts for one campaign.

**Limitation:** 

- In the DEMO account mode, creating a campaign via API is not available.
- In the TEST platform mode, creating a campaign is possible only for the verified numbers.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.sms_campaign_response import SmsCampaignResponse
from bsg_api.models.sms_send_groups_request import SmsSendGroupsRequest
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
    api_instance = bsg_api.CampaignSMSApi(api_client)
    sms_send_groups_request = {"groups":[1864275],"text":"hello!","sender":"Vet klinika"} # SmsSendGroupsRequest | 

    try:
        # Send SMS to contact list
        api_response = api_instance.sms_send_groups(sms_send_groups_request)
        print("The response of CampaignSMSApi->sms_send_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignSMSApi->sms_send_groups: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sms_send_groups_request** | [**SmsSendGroupsRequest**](SmsSendGroupsRequest.md) |  |  |

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
    api_instance = bsg_api.CampaignSMSApi(api_client)
    sms_send_individual_request = {"messages":[{"phone":380661231231,"text":"hello Jack","sender":"Vet klinika"},{"phone":380661231232,"text":"hello Anna","sender":"Vet klinika"},{"phone":380661231233,"text":"Hi Hellen","sender":"Vet klinika"}]} # SmsSendIndividualRequest | 

    try:
        # Send SMS with different text
        api_response = api_instance.sms_send_individual(sms_send_individual_request)
        print("The response of CampaignSMSApi->sms_send_individual:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignSMSApi->sms_send_individual: %s\n" % e)
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

