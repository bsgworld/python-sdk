# bsg_api.CampaignApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**campaign**](CampaignApi.md#campaign) | **GET** /api/campaigns/{id} | Get campaign info |
| [**campaign_details**](CampaignApi.md#campaign_details) | **GET** /api/campaigns/{id}/detail | Get campaign details |
| [**campaign_price**](CampaignApi.md#campaign_price) | **POST** /api/campaigns/price | Calculate campaign price |
| [**campaign_stop**](CampaignApi.md#campaign_stop) | **PATCH** /api/campaigns/{id}/stop | Cancel campaign |
| [**campaigns**](CampaignApi.md#campaigns) | **GET** /api/campaigns | List of campaigns |


# **campaign**
> Campaign200Response campaign(id)

Get campaign info

Retrieve campaign with all it’s properties

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.campaign200_response import Campaign200Response
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
    api_instance = bsg_api.CampaignApi(api_client)
    id = 53651994 # int | 

    try:
        # Get campaign info
        api_response = api_instance.campaign(id)
        print("The response of CampaignApi->campaign:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignApi->campaign: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |

### Return type

[**Campaign200Response**](Campaign200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Campaign info |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = bsg_api.CampaignApi(api_client)
    id = 53651994 # int | 

    try:
        # Get campaign details
        api_response = api_instance.campaign_details(id)
        print("The response of CampaignApi->campaign_details:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignApi->campaign_details: %s\n" % e)
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
    api_instance = bsg_api.CampaignApi(api_client)
    campaign_price_request = {"sender":"Vet klinika","text":"hello!","messages":[{"phone":38267161234}]} # CampaignPriceRequest | 

    try:
        # Calculate campaign price
        api_response = api_instance.campaign_price(campaign_price_request)
        print("The response of CampaignApi->campaign_price:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignApi->campaign_price: %s\n" % e)
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

# **campaign_stop**
> CampaignStop200Response campaign_stop(id)

Cancel campaign

Abort the campaign and move it to finally status stopped

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.campaign_stop200_response import CampaignStop200Response
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
    api_instance = bsg_api.CampaignApi(api_client)
    id = 56 # int | 

    try:
        # Cancel campaign
        api_response = api_instance.campaign_stop(id)
        print("The response of CampaignApi->campaign_stop:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignApi->campaign_stop: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |

### Return type

[**CampaignStop200Response**](CampaignStop200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |
| **422** | Invalid campaign status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = bsg_api.CampaignApi(api_client)
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
        print("The response of CampaignApi->campaigns:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CampaignApi->campaigns: %s\n" % e)
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

