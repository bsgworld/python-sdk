# bsg_api.ContactFieldApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contact_field_create**](ContactFieldApi.md#contact_field_create) | **POST** /api/contacts/fields | Create contact field |
| [**contact_field_update**](ContactFieldApi.md#contact_field_update) | **PATCH** /api/contacts/fields/{id} | Update contact field |
| [**contact_fields**](ContactFieldApi.md#contact_fields) | **GET** /api/contacts/fields | List of contact fields |
| [**post_contacts_fields_delete**](ContactFieldApi.md#post_contacts_fields_delete) | **POST** /api/contacts/fields/delete | Delete contact fields by ids |


# **contact_field_create**
> ContactFieldCreate201Response contact_field_create(contact_field_create_request)

Create contact field

The method allows the creation of additional custom fields for contacts

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_field_create201_response import ContactFieldCreate201Response
from bsg_api.models.contact_field_create_request import ContactFieldCreateRequest
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
    api_instance = bsg_api.ContactFieldApi(api_client)
    contact_field_create_request = bsg_api.ContactFieldCreateRequest() # ContactFieldCreateRequest | 

    try:
        # Create contact field
        api_response = api_instance.contact_field_create(contact_field_create_request)
        print("The response of ContactFieldApi->contact_field_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldApi->contact_field_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_field_create_request** | [**ContactFieldCreateRequest**](ContactFieldCreateRequest.md) |  |  |

### Return type

[**ContactFieldCreate201Response**](ContactFieldCreate201Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **201** | Successful created |  -  |
| **429** | Too many requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_field_update**
> ContactFieldUpdate200Response contact_field_update(id, contact_field_update_request)

Update contact field

Method for editing custom contact field:

- change field name
- change field description


### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_field_update200_response import ContactFieldUpdate200Response
from bsg_api.models.contact_field_update_request import ContactFieldUpdateRequest
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
    api_instance = bsg_api.ContactFieldApi(api_client)
    id = 56 # int | Contact field id
    contact_field_update_request = bsg_api.ContactFieldUpdateRequest() # ContactFieldUpdateRequest | 

    try:
        # Update contact field
        api_response = api_instance.contact_field_update(id, contact_field_update_request)
        print("The response of ContactFieldApi->contact_field_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldApi->contact_field_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact field id |  |
| **contact_field_update_request** | [**ContactFieldUpdateRequest**](ContactFieldUpdateRequest.md) |  |  |

### Return type

[**ContactFieldUpdate200Response**](ContactFieldUpdate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_fields**
> ContactFieldCollectionSchema contact_fields()

List of contact fields

Get a list of custom fields

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.contact_field_collection_schema import ContactFieldCollectionSchema
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
    api_instance = bsg_api.ContactFieldApi(api_client)

    try:
        # List of contact fields
        api_response = api_instance.contact_fields()
        print("The response of ContactFieldApi->contact_fields:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldApi->contact_fields: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ContactFieldCollectionSchema**](ContactFieldCollectionSchema.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Contact field list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_contacts_fields_delete**
> object post_contacts_fields_delete(post_contacts_fields_delete_request)

Delete contact fields by ids

Delete multiple (up to 30) contact fields

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.post_contacts_fields_delete_request import PostContactsFieldsDeleteRequest
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
    api_instance = bsg_api.ContactFieldApi(api_client)
    post_contacts_fields_delete_request = bsg_api.PostContactsFieldsDeleteRequest() # PostContactsFieldsDeleteRequest | 

    try:
        # Delete contact fields by ids
        api_response = api_instance.post_contacts_fields_delete(post_contacts_fields_delete_request)
        print("The response of ContactFieldApi->post_contacts_fields_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactFieldApi->post_contacts_fields_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_contacts_fields_delete_request** | [**PostContactsFieldsDeleteRequest**](PostContactsFieldsDeleteRequest.md) |  |  |

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
| **204** | Successful removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

