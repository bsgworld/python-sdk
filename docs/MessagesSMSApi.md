# bsg_api.MessagesSMSApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_messages**](MessagesSMSApi.md#get_messages) | **GET** /api/messages | Find messages |


# **get_messages**
> GetMessages200Response get_messages(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, filter_id=filter_id, filter_campaign_id=filter_campaign_id, filter_reference_id=filter_reference_id, filter_from=filter_from, filter_to=filter_to)

Find messages

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.get_messages200_response import GetMessages200Response
from bsg_api.models.sort_way import SortWay
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
    api_instance = bsg_api.MessagesSMSApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)
    sort = id # str | Field to sort the results (optional) (default to id)
    way = asc # SortWay |  (optional) (default to asc)
    filter_id = 56 # int |  (optional)
    filter_campaign_id = 56 # int | Filter by campaign Id received when [send message](#operation/sms_send) (optional)
    filter_reference_id = 'filter_reference_id_example' # str | Filter by reference passed when [send message](#operation/sms_send) (optional)
    filter_from = '2025-03-20 00:00:00' # datetime | Filter message from this date. format ― Y-m-d H:i:s (optional)
    filter_to = '2025-03-31 00:00:00' # datetime | Filter message up to this date. format ― Y-m-d H:i:s (optional)

    try:
        # Find messages
        api_response = api_instance.get_messages(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, filter_id=filter_id, filter_campaign_id=filter_campaign_id, filter_reference_id=filter_reference_id, filter_from=filter_from, filter_to=filter_to)
        print("The response of MessagesSMSApi->get_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MessagesSMSApi->get_messages: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **str** | Field to sort the results | [optional] [default to id] |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **filter_id** | **int** |  | [optional]  |
| **filter_campaign_id** | **int** | Filter by campaign Id received when [send message](#operation/sms_send) | [optional]  |
| **filter_reference_id** | **str** | Filter by reference passed when [send message](#operation/sms_send) | [optional]  |
| **filter_from** | **datetime** | Filter message from this date. format ― Y-m-d H:i:s | [optional]  |
| **filter_to** | **datetime** | Filter message up to this date. format ― Y-m-d H:i:s | [optional]  |

### Return type

[**GetMessages200Response**](GetMessages200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

