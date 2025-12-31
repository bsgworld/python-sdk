# bsg_api.ShortDomainsApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_domain**](ShortDomainsApi.md#short_urls_domain) | **GET** /api/short-url/domains/{uuid} | Get domain by uuid |
| [**short_urls_domain_create**](ShortDomainsApi.md#short_urls_domain_create) | **POST** /api/short-url/domains | Add domain |
| [**short_urls_domain_remove**](ShortDomainsApi.md#short_urls_domain_remove) | **DELETE** /api/short-url/domains/{uuid} | Remove domain |
| [**short_urls_domain_update**](ShortDomainsApi.md#short_urls_domain_update) | **PUT** /api/short-url/domains/{uuid} | Update domain |
| [**short_urls_domains**](ShortDomainsApi.md#short_urls_domains) | **GET** /api/short-url/domains | List of domains |


# **short_urls_domain**
> ShortUrlsDomain200Response short_urls_domain(uuid)

Get domain by uuid

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_domain200_response import ShortUrlsDomain200Response
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
    api_instance = bsg_api.ShortDomainsApi(api_client)
    uuid = 'db05af9e-107e-4ed6-b1ac-a373d90109c8' # str | Uuid of entity

    try:
        # Get domain by uuid
        api_response = api_instance.short_urls_domain(uuid)
        print("The response of ShortDomainsApi->short_urls_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortDomainsApi->short_urls_domain: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |

### Return type

[**ShortUrlsDomain200Response**](ShortUrlsDomain200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |
| **422** | Domain not found. Pass correct domain uuid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **short_urls_domain_create**
> ShortUrlsDomainCreate201Response short_urls_domain_create(domain_store_request=domain_store_request)

Add domain

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.domain_store_request import DomainStoreRequest
from bsg_api.models.short_urls_domain_create201_response import ShortUrlsDomainCreate201Response
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
    api_instance = bsg_api.ShortDomainsApi(api_client)
    domain_store_request = {"name":"short.ai","slug_type":"random"} # DomainStoreRequest |  (optional)

    try:
        # Add domain
        api_response = api_instance.short_urls_domain_create(domain_store_request=domain_store_request)
        print("The response of ShortDomainsApi->short_urls_domain_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortDomainsApi->short_urls_domain_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain_store_request** | [**DomainStoreRequest**](DomainStoreRequest.md) |  | [optional]  |

### Return type

[**ShortUrlsDomainCreate201Response**](ShortUrlsDomainCreate201Response.md)

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

# **short_urls_domain_remove**
> object short_urls_domain_remove(uuid)

Remove domain

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
    api_instance = bsg_api.ShortDomainsApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity

    try:
        # Remove domain
        api_response = api_instance.short_urls_domain_remove(uuid)
        print("The response of ShortDomainsApi->short_urls_domain_remove:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortDomainsApi->short_urls_domain_remove: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |

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
| **422** | Domain not found. Pass correct domain uuid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **short_urls_domain_update**
> ShortUrlsDomainUpdate200Response short_urls_domain_update(uuid, domain_update_request)

Update domain

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.domain_update_request import DomainUpdateRequest
from bsg_api.models.short_urls_domain_update200_response import ShortUrlsDomainUpdate200Response
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
    api_instance = bsg_api.ShortDomainsApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity
    domain_update_request = {"is_default":true} # DomainUpdateRequest | 

    try:
        # Update domain
        api_response = api_instance.short_urls_domain_update(uuid, domain_update_request)
        print("The response of ShortDomainsApi->short_urls_domain_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortDomainsApi->short_urls_domain_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |
| **domain_update_request** | [**DomainUpdateRequest**](DomainUpdateRequest.md) |  |  |

### Return type

[**ShortUrlsDomainUpdate200Response**](ShortUrlsDomainUpdate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successfully updated |  -  |
| **422** | Domain not found. Pass correct domain uuid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **short_urls_domains**
> ShortUrlsDomains200Response short_urls_domains(var_from, to, page=page, per_page=per_page)

List of domains

Get list of short urls domains

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_domains200_response import ShortUrlsDomains200Response
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
    api_instance = bsg_api.ShortDomainsApi(api_client)
    var_from = '2022-04-28' # str | From date
    to = '2022-04-28' # str | To date
    page = 1 # int | Get items starting from this page. (optional) (default to 1)
    per_page = 20 # int | The number of items in the page. Possible values are from 10 to 500. (optional) (default to 20)

    try:
        # List of domains
        api_response = api_instance.short_urls_domains(var_from, to, page=page, per_page=per_page)
        print("The response of ShortDomainsApi->short_urls_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortDomainsApi->short_urls_domains: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_from** | **str** | From date |  |
| **to** | **str** | To date |  |
| **page** | **int** | Get items starting from this page. | [optional] [default to 1] |
| **per_page** | **int** | The number of items in the page. Possible values are from 10 to 500. | [optional] [default to 20] |

### Return type

[**ShortUrlsDomains200Response**](ShortUrlsDomains200Response.md)

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

