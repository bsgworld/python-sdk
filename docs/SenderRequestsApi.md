# bsg_api.SenderRequestsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**sender_requests**](SenderRequestsApi.md#sender_requests) | **GET** /api/senders/requests/sms | List of Sender Requests |


# **sender_requests**
> SenderRequests200Response sender_requests(page_limit=page_limit, page_offset=page_offset, sort=sort, way=way, filter_status=filter_status, filter_id=filter_id, filter_country_code=filter_country_code, filter_sender=filter_sender, filter_created_at=filter_created_at)

List of Sender Requests

Get SMS Senders request status

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.sender_request_status import SenderRequestStatus
from bsg_api.models.sender_requests200_response import SenderRequests200Response
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
    api_instance = bsg_api.SenderRequestsApi(api_client)
    page_limit = 50 # int |  (optional) (default to 50)
    page_offset = 0 # int |  (optional) (default to 0)
    sort = id # str |  (optional) (default to id)
    way = asc # SortWay |  (optional) (default to asc)
    filter_status = bsg_api.SenderRequestStatus() # SenderRequestStatus |  (optional)
    filter_id = 56 # int |  (optional)
    filter_country_code = 'filter_country_code_example' # str |  (optional)
    filter_sender = 'filter_sender_example' # str |  (optional)
    filter_created_at = '2013-10-20T19:20:30+01:00' # datetime |  (optional)

    try:
        # List of Sender Requests
        api_response = api_instance.sender_requests(page_limit=page_limit, page_offset=page_offset, sort=sort, way=way, filter_status=filter_status, filter_id=filter_id, filter_country_code=filter_country_code, filter_sender=filter_sender, filter_created_at=filter_created_at)
        print("The response of SenderRequestsApi->sender_requests:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SenderRequestsApi->sender_requests: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_limit** | **int** |  | [optional] [default to 50] |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **sort** | **str** |  | [optional] [default to id] |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **filter_status** | [**SenderRequestStatus**](.md) |  | [optional]  |
| **filter_id** | **int** |  | [optional]  |
| **filter_country_code** | **str** |  | [optional]  |
| **filter_sender** | **str** |  | [optional]  |
| **filter_created_at** | **datetime** |  | [optional]  |

### Return type

[**SenderRequests200Response**](SenderRequests200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Sender requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

