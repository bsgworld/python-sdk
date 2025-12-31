# bsg_api.ContactListApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_list**](ContactListApi.md#contact_list) | **GET** /api/groups/{id} | Get list by id |
| [**contact_list_attach**](ContactListApi.md#contact_list_attach) | **POST** /api/groups/attach | Add contacts to the list |
| [**contact_list_create**](ContactListApi.md#contact_list_create) | **POST** /api/groups | Create list |
| [**contact_list_delete**](ContactListApi.md#contact_list_delete) | **DELETE** /api/groups/{id} | Delete list |
| [**contact_list_detach**](ContactListApi.md#contact_list_detach) | **POST** /api/groups/detach | Remove contacts from the list |
| [**contact_list_search**](ContactListApi.md#contact_list_search) | **GET** /api/groups/search | Search list |
| [**contact_list_update**](ContactListApi.md#contact_list_update) | **PUT** /api/groups/{id} | Update list |
| [**contact_lists**](ContactListApi.md#contact_lists) | **GET** /api/groups | List of contact lists |


# **contact_list**
> ContactList200Response contact_list(id)

Get list by id

Get information about the contact list by its identifier

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list200_response import ContactList200Response
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
    api_instance = bsg_api.ContactListApi(api_client)
    id = 56 # int | 

    try:
        # Get list by id
        api_response = api_instance.contact_list(id)
        print("The response of ContactListApi->contact_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |

### Return type

[**ContactList200Response**](ContactList200Response.md)

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

# **contact_list_attach**
> object contact_list_attach(contact_list_attach_request)

Add contacts to the list

The method provides the ability to add an existing contact to the list. The action can be single or bulk.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_attach_request import ContactListAttachRequest
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
    api_instance = bsg_api.ContactListApi(api_client)
    contact_list_attach_request = {"contacts":[248452959,248452739,248452740],"groups":[1864623,1864621]} # ContactListAttachRequest | 

    try:
        # Add contacts to the list
        api_response = api_instance.contact_list_attach(contact_list_attach_request)
        print("The response of ContactListApi->contact_list_attach:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list_attach: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_list_attach_request** | [**ContactListAttachRequest**](ContactListAttachRequest.md) |  |  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful attached |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_list_create**
> ContactListCreate201Response contact_list_create(contact_list_create_request)

Create list

Create a contact list to group contacts

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_create201_response import ContactListCreate201Response
from bsg_api.models.contact_list_create_request import ContactListCreateRequest
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
    api_instance = bsg_api.ContactListApi(api_client)
    contact_list_create_request = {"name":"new list 123"} # ContactListCreateRequest | 

    try:
        # Create list
        api_response = api_instance.contact_list_create(contact_list_create_request)
        print("The response of ContactListApi->contact_list_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_list_create_request** | [**ContactListCreateRequest**](ContactListCreateRequest.md) |  |  |

### Return type

[**ContactListCreate201Response**](ContactListCreate201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **422** | Error |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_list_delete**
> contact_list_delete(id)

Delete list

Method for deleting contact list. Please note that when you delete a contact list, all contacts that were added to it are not deleted from your Contact Book

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
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
    api_instance = bsg_api.ContactListApi(api_client)
    id = 56 # int | 

    try:
        # Delete list
        api_instance.contact_list_delete(id)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |

### Return type

void (empty response body)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_list_detach**
> object contact_list_detach(contact_list_detach_request)

Remove contacts from the list

Performs the removal of contact from the list. The action can be single (string) or bulk (array)

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_detach_request import ContactListDetachRequest
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
    api_instance = bsg_api.ContactListApi(api_client)
    contact_list_detach_request = {"contacts":[248452959,248452739,248452740],"groups":[1864623,1864621]} # ContactListDetachRequest | 

    try:
        # Remove contacts from the list
        api_response = api_instance.contact_list_detach(contact_list_detach_request)
        print("The response of ContactListApi->contact_list_detach:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list_detach: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_list_detach_request** | [**ContactListDetachRequest**](ContactListDetachRequest.md) |  |  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful detached |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = bsg_api.ContactListApi(api_client)
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
        print("The response of ContactListApi->contact_list_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list_search: %s\n" % e)
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

# **contact_list_update**
> ContactListUpdate200Response contact_list_update(id, contact_list_update_request)

Update list

Performs editing of the selected contacts list

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_list_update200_response import ContactListUpdate200Response
from bsg_api.models.contact_list_update_request import ContactListUpdateRequest
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
    api_instance = bsg_api.ContactListApi(api_client)
    id = 56 # int | 
    contact_list_update_request = bsg_api.ContactListUpdateRequest() # ContactListUpdateRequest | 

    try:
        # Update list
        api_response = api_instance.contact_list_update(id, contact_list_update_request)
        print("The response of ContactListApi->contact_list_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_list_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  |  |
| **contact_list_update_request** | [**ContactListUpdateRequest**](ContactListUpdateRequest.md) |  |  |

### Return type

[**ContactListUpdate200Response**](ContactListUpdate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful updated |  -  |
| **422** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_lists**
> ContactLists200Response contact_lists(page_offset=page_offset, page_limit=page_limit)

List of contact lists

Provides an index of all the contact lists with data

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_lists200_response import ContactLists200Response
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
    api_instance = bsg_api.ContactListApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 50 # int | The number of items in the response (optional) (default to 50)

    try:
        # List of contact lists
        api_response = api_instance.contact_lists(page_offset=page_offset, page_limit=page_limit)
        print("The response of ContactListApi->contact_lists:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactListApi->contact_lists: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |

### Return type

[**ContactLists200Response**](ContactLists200Response.md)

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

