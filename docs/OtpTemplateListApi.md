# bsg_api.OtpTemplateListApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**otp_template_list**](OtpTemplateListApi.md#otp_template_list) | **GET** /api/2fa/authentications/templates | List of message templates |


# **otp_template_list**
> OtpTemplateList200Response otp_template_list(page_offset=page_offset, page_limit=page_limit, filter_ids=filter_ids, filter_status=filter_status, sort=sort, way=way)

List of message templates

This method returns a list of message templates for sending OTR code, allowing you to filter them by various parameters.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.otp_template_list200_response import OtpTemplateList200Response
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
    api_instance = bsg_api.OtpTemplateListApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 10 # int |  (optional) (default to 10)
    filter_ids = [56] # List[int] |  (optional)
    filter_status = 'filter_status_example' # str |  (optional)
    sort = template_id # str | Sorting by (optional) (default to template_id)
    way = asc # SortWay |  (optional) (default to asc)

    try:
        # List of message templates
        api_response = api_instance.otp_template_list(page_offset=page_offset, page_limit=page_limit, filter_ids=filter_ids, filter_status=filter_status, sort=sort, way=way)
        print("The response of OtpTemplateListApi->otp_template_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OtpTemplateListApi->otp_template_list: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** |  | [optional] [default to 10] |
| **filter_ids** | [**List[int]**](int.md) |  | [optional]  |
| **filter_status** | **str** |  | [optional]  |
| **sort** | **str** | Sorting by | [optional] [default to template_id] |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |

### Return type

[**OtpTemplateList200Response**](OtpTemplateList200Response.md)

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

