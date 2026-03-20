# bsg_api.OtpListApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**otp_list**](OtpListApi.md#otp_list) | **GET** /api/2fa/authentications | List of authentication sessions |


# **otp_list**
> OtpList200Response otp_list(filter_from, filter_to, page_offset=page_offset, page_limit=page_limit, filter_ids=filter_ids, filter_status=filter_status, filter_channel=filter_channel, filter_recipient=filter_recipient, filter_country_code=filter_country_code, way=way, sort=sort)

List of authentication sessions

Use to get a list of authentications for a period.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.otp_channel import OtpChannel
from bsg_api.models.otp_list200_response import OtpList200Response
from bsg_api.models.otp_status import OtpStatus
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
    api_instance = bsg_api.OtpListApi(api_client)
    filter_from = 'Thu Dec 01 00:00:00 UTC 2022' # date | Period start date (date and time when the authentication session was created) in ISO 8601 format.
    filter_to = 'Sat Dec 31 00:00:00 UTC 2022' # date | End date of the period (date and time when the authentication was created) in ISO 8601 format.
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 10 # int |  (optional) (default to 10)
    filter_ids = ['filter_ids_example'] # List[str] | Authentication ID. The maximum number is 3. (optional)
    filter_status = bsg_api.OtpStatus() # OtpStatus |  (optional)
    filter_channel = bsg_api.OtpChannel() # OtpChannel |  (optional)
    filter_recipient = 'filter_recipient_example' # str |  (optional)
    filter_country_code = 'filter_country_code_example' # str |  (optional)
    way = asc # SortWay |  (optional) (default to asc)
    sort = id # str | Sort by (optional) (default to id)

    try:
        # List of authentication sessions
        api_response = api_instance.otp_list(filter_from, filter_to, page_offset=page_offset, page_limit=page_limit, filter_ids=filter_ids, filter_status=filter_status, filter_channel=filter_channel, filter_recipient=filter_recipient, filter_country_code=filter_country_code, way=way, sort=sort)
        print("The response of OtpListApi->otp_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OtpListApi->otp_list: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filter_from** | **date** | Period start date (date and time when the authentication session was created) in ISO 8601 format. |  |
| **filter_to** | **date** | End date of the period (date and time when the authentication was created) in ISO 8601 format. |  |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** |  | [optional] [default to 10] |
| **filter_ids** | [**List[str]**](str.md) | Authentication ID. The maximum number is 3. | [optional]  |
| **filter_status** | [**OtpStatus**](.md) |  | [optional]  |
| **filter_channel** | [**OtpChannel**](.md) |  | [optional]  |
| **filter_recipient** | **str** |  | [optional]  |
| **filter_country_code** | **str** |  | [optional]  |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **sort** | **str** | Sort by | [optional] [default to id] |

### Return type

[**OtpList200Response**](OtpList200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation: TwoFA authentications list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

