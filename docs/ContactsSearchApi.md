# bsg_api.ContactsSearchApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contacts_search**](ContactsSearchApi.md#contacts_search) | **GET** /api/contacts/search | Search contacts |


# **contacts_search**
> ContactsSearch200Response contacts_search(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, search_field=search_field, search_operator=search_operator, search_value=search_value, search_fields_0_field=search_fields_0_field, search_fields_0_operator=search_fields_0_operator, search_fields_0_value=search_fields_0_value)

Search contacts

Method for searching contacts in the Contact Book. In the search, it is possible to use operations: like, =, >, >=, <, <=.

Search is possible by the following fields: 

- id:  =, >, >=, <, <=
- phone: like, =
- {field_id}:
  - for field with "Text" type: like, =
  - for field with "Number" type:  =, >, >=, <, <=
  - for field with "Date" type: =, >, >=, <, <=

It’s possible to pass multiple criteria by pass `search_fields` array instead of `search`


### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contacts_search200_response import ContactsSearch200Response
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
    api_instance = bsg_api.ContactsSearchApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)
    sort = id # str | Sort by conditions: id, phone (optional) (default to id)
    way = asc # SortWay |  (optional) (default to asc)
    search_field = 'search_field_example' # str |  (optional)
    search_operator = bsg_api.SearchOperator() # SearchOperator |  (optional)
    search_value = 'search_value_example' # str |  (optional)
    search_fields_0_field = 'search_fields_0_field_example' # str |  (optional)
    search_fields_0_operator = bsg_api.SearchOperator() # SearchOperator |  (optional)
    search_fields_0_value = 'search_fields_0_value_example' # str |  (optional)

    try:
        # Search contacts
        api_response = api_instance.contacts_search(page_offset=page_offset, page_limit=page_limit, sort=sort, way=way, search_field=search_field, search_operator=search_operator, search_value=search_value, search_fields_0_field=search_fields_0_field, search_fields_0_operator=search_fields_0_operator, search_fields_0_value=search_fields_0_value)
        print("The response of ContactsSearchApi->contacts_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsSearchApi->contacts_search: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **str** | Sort by conditions: id, phone | [optional] [default to id] |
| **way** | [**SortWay**](.md) |  | [optional] [default to asc] |
| **search_field** | **str** |  | [optional]  |
| **search_operator** | [**SearchOperator**](.md) |  | [optional]  |
| **search_value** | **str** |  | [optional]  |
| **search_fields_0_field** | **str** |  | [optional]  |
| **search_fields_0_operator** | [**SearchOperator**](.md) |  | [optional]  |
| **search_fields_0_value** | **str** |  | [optional]  |

### Return type

[**ContactsSearch200Response**](ContactsSearch200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Searched contacts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

