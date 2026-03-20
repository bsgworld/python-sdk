# bsg_api.CampaignsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**campaigns**](CampaignsApi.md#campaigns) | **GET** /api/campaigns | List of campaigns |


# **campaigns**
> SearchCampaignResource campaigns(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, filter_from=filter_from, filter_to=filter_to, filter_type=filter_type, search_field=search_field, search_value=search_value)

List of campaigns

Get a list of campaigns based on specified criteria

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.search_campaign_resource import SearchCampaignResource
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
    api_instance = bsg_api.CampaignsApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)
    sort = id # str | Sort items by (optional) (default to id)
    way = asc # SortWay |  (optional) (default to asc)
    filter_from = '2013-10-20T19:20:30+01:00' # datetime | Include items from (optional)
    filter_to = '2013-10-20T19:20:30+01:00' # datetime | Include items to (optional)
    filter_type = 'filter_type_example' # str | Filter items by type type (optional)
    search_field = 'search_field_example' # str | Filter items by search[field]=search[value] (optional)
    search_value = 'search_value_example' # str | Filter items by search[field]=search[value] (optional)

    try:
        # List of campaigns
        api_response = api_instance.campaigns(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, filter_from=filter_from, filter_to=filter_to, filter_type=filter_type, search_field=search_field, search_value=search_value)
        print("The response of CampaignsApi->campaigns:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignsApi->campaigns: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **str** | Sort items by | [optional] [default to id] |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **filter_from** | **datetime** | Include items from | [optional]  |
| **filter_to** | **datetime** | Include items to | [optional]  |
| **filter_type** | **str** | Filter items by type type | [optional]  |
| **search_field** | **str** | Filter items by search[field]&#x3D;search[value] | [optional]  |
| **search_value** | **str** | Filter items by search[field]&#x3D;search[value] | [optional]  |

### Return type

[**SearchCampaignResource**](SearchCampaignResource.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Paginated list of campaigns |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

