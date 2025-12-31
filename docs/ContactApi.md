# bsg_api.ContactApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact**](ContactApi.md#contact) | **GET** /api/contacts/{id} | Get contact by ID |
| [**contact_create**](ContactApi.md#contact_create) | **POST** /api/contacts | Create a contact |
| [**contact_delete**](ContactApi.md#contact_delete) | **DELETE** /api/contacts/{id} | Delete contact |
| [**contact_update**](ContactApi.md#contact_update) | **PUT** /api/contacts/{id} | Update contact |
| [**contacts**](ContactApi.md#contacts) | **GET** /api/contacts | List of contacts |
| [**contacts_delete**](ContactApi.md#contacts_delete) | **POST** /api/contacts/delete | Delete multiple contacts |
| [**contacts_search**](ContactApi.md#contacts_search) | **GET** /api/contacts/search | Search contacts |


# **contact**
> Contact200Response contact(id)

Get contact by ID

The method allows you to receive detailed information about an existing contact, which is contained in the system, and user fields of the contact

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact200_response import Contact200Response
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
    api_instance = bsg_api.ContactApi(api_client)
    id = 248452739 # int | Contact id

    try:
        # Get contact by ID
        api_response = api_instance.contact(id)
        print("The response of ContactApi->contact:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contact: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact id |  |

### Return type

[**Contact200Response**](Contact200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Contact object |  -  |
| **422** | Invalid contact id |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_create**
> ContactCreate201Response contact_create(store_contact)

Create a contact

The method allows adding new contacts to your Contact Book. 

**Please note:** that in the TEST account mode there is a restriction for performing this method: it is possible to create a contact only for a verified phone number (number verification is performed in the personal account of the platform).

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_create201_response import ContactCreate201Response
from bsg_api.models.store_contact import StoreContact
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
    api_instance = bsg_api.ContactApi(api_client)
    store_contact = {"phone":61401629754} # StoreContact | 

    try:
        # Create a contact
        api_response = api_instance.contact_create(store_contact)
        print("The response of ContactApi->contact_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contact_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **store_contact** | [**StoreContact**](StoreContact.md) |  |  |

### Return type

[**ContactCreate201Response**](ContactCreate201Response.md)

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

# **contact_delete**
> object contact_delete(id)

Delete contact

Use this query to remove an existing contact from the Contact Book. When this query is made, the contact will also be removed from all lists where it was added.

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
    api_instance = bsg_api.ContactApi(api_client)
    id = 56 # int | Contact id

    try:
        # Delete contact
        api_response = api_instance.contact_delete(id)
        print("The response of ContactApi->contact_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contact_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact id |  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_update**
> ContactUpdate200Response contact_update(id, contact_update_request)

Update contact

The method allows you to make changes to an existing contact: change the phone number, data in the contact’s custom fields, and add the contact to the list.

**Please note:** that in the TEST account mode there is a restriction for performing this method: you can only change the contact’s phone number to a verified number (number verification is performed in the personal account at the platform)

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_update200_response import ContactUpdate200Response
from bsg_api.models.contact_update_request import ContactUpdateRequest
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
    api_instance = bsg_api.ContactApi(api_client)
    id = 56 # int | Contact id
    contact_update_request = {"phone":61401629754,"fields":[{"id":387714,"value":"Ilya Muromets"}],"groups":[1864618]} # ContactUpdateRequest | 

    try:
        # Update contact
        api_response = api_instance.contact_update(id, contact_update_request)
        print("The response of ContactApi->contact_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contact_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact id |  |
| **contact_update_request** | [**ContactUpdateRequest**](ContactUpdateRequest.md) |  |  |

### Return type

[**ContactUpdate200Response**](ContactUpdate200Response.md)

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

# **contacts**
> Contacts200Response contacts(page_offset=page_offset, page_limit=page_limit, groups=groups)

List of contacts

Get a list of existing contacts in the Contact Book of your account with detailed information on each of them. The method also allows you to get contacts from the certain lists that you specified in the query parameters.

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contacts200_response import Contacts200Response
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
    api_instance = bsg_api.ContactApi(api_client)
    page_offset = 0 # int |  (optional) (default to 0)
    page_limit = 20 # int | The number of items in the response (optional) (default to 20)
    groups = [[1864618]] # List[int] | Index of IDs of the lists for which you want to display contacts (optional)

    try:
        # List of contacts
        api_response = api_instance.contacts(page_offset=page_offset, page_limit=page_limit, groups=groups)
        print("The response of ContactApi->contacts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contacts: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 20] |
| **groups** | [**List[int]**](int.md) | Index of IDs of the lists for which you want to display contacts | [optional]  |

### Return type

[**Contacts200Response**](Contacts200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Paginated list of contacts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contacts_delete**
> object contacts_delete(contact_ids=contact_ids, group_ids=group_ids)

Delete multiple contacts

Method allow to delete multiple contacts (up to 5000) for a single request

It may be list of contact ids to delete or list of contact lists ids to delete **contacts** included into these lists.


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
    api_instance = bsg_api.ContactApi(api_client)
    contact_ids = [56] # List[int] | Contact ids to delete (optional)
    group_ids = [56] # List[int] | Contact lists ids to delete **contacts** included into these lists (optional)

    try:
        # Delete multiple contacts
        api_response = api_instance.contacts_delete(contact_ids=contact_ids, group_ids=group_ids)
        print("The response of ContactApi->contacts_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contacts_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_ids** | [**List[int]**](int.md) | Contact ids to delete | [optional]  |
| **group_ids** | [**List[int]**](int.md) | Contact lists ids to delete **contacts** included into these lists | [optional]  |

### Return type

**object**

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = bsg_api.ContactApi(api_client)
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
        print("The response of ContactApi->contacts_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactApi->contacts_search: %s\n" % e)
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

