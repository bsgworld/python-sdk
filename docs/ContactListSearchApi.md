# bsg_api.ContactListSearchApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list_search**](ContactListSearchApi.md#contact_list_search) | **GET** /api/groups/search | Search list |


# **contact_list_search**
> ContactListSearch200Response contact_list_search(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, search_field=search_field, search_operator=search_operator, search_value=search_value, search_fields_0_field=search_fields_0_field, search_fields_0_operator=search_fields_0_operator, search_fields_0_value=search_fields_0_value)

Search list

Method for searching the list of contacts using operations like, =, >, >=, <, <=.
Search is possible by the following fields: 

- name
- description
- date
- items
- phone
- id


### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_group_search_field import ContactGroupSearchField
from bsg_api.models.contact_list_search200_response import ContactListSearch200Response
from bsg_api.models.search_operator import SearchOperator
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
    api_instance = bsg_api.ContactListSearchApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)
    sort = id # str |  (optional) (default to id)
    way = asc # SortWay |  (optional) (default to asc)
    search_field = bsg_api.ContactGroupSearchField() # ContactGroupSearchField |  (optional)
    search_operator = bsg_api.SearchOperator() # SearchOperator |  (optional)
    search_value = 'search_value_example' # str |  (optional)
    search_fields_0_field = bsg_api.ContactGroupSearchField() # ContactGroupSearchField |  (optional)
    search_fields_0_operator = bsg_api.SearchOperator() # SearchOperator |  (optional)
    search_fields_0_value = 'search_fields_0_value_example' # str |  (optional)

    try:
        # Search list
        api_response = api_instance.contact_list_search(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, search_field=search_field, search_operator=search_operator, search_value=search_value, search_fields_0_field=search_fields_0_field, search_fields_0_operator=search_fields_0_operator, search_fields_0_value=search_fields_0_value)
        print("The response of ContactListSearchApi->contact_list_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListSearchApi->contact_list_search: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **str** |  | [optional] [default to id] |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **search_field** | [**ContactGroupSearchField**](.md) |  | [optional]  |
| **search_operator** | [**SearchOperator**](.md) |  | [optional]  |
| **search_value** | **str** |  | [optional]  |
| **search_fields_0_field** | [**ContactGroupSearchField**](.md) |  | [optional]  |
| **search_fields_0_operator** | [**SearchOperator**](.md) |  | [optional]  |
| **search_fields_0_value** | **str** |  | [optional]  |

### Return type

[**ContactListSearch200Response**](ContactListSearch200Response.md)

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

