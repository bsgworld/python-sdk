# bsg_api.ContactsDeleteApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**contacts_delete**](ContactsDeleteApi.md#contacts_delete) | **POST** /api/contacts/delete | Delete multiple contacts |


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
    api_instance = bsg_api.ContactsDeleteApi(api_client)
    contact_ids = [56] # List[int] | Contact ids to delete (optional)
    group_ids = [56] # List[int] | Contact lists ids to delete **contacts** included into these lists (optional)

    try:
        # Delete multiple contacts
        api_response = api_instance.contacts_delete(contact_ids=contact_ids, group_ids=group_ids)
        print("The response of ContactsDeleteApi->contacts_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactsDeleteApi->contacts_delete: %s\n" % e)
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

