# bsg_api.StatisticApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**stat_jobs_create**](StatisticApi.md#stat_jobs_create) | **POST** /api/stat/jobs | Create new job |
| [**stat_jobs_delete**](StatisticApi.md#stat_jobs_delete) | **DELETE** /api/stat/jobs/{id} | Delete job result |
| [**stat_jobs_list**](StatisticApi.md#stat_jobs_list) | **GET** /api/stat/jobs | List statistic jobs |
| [**stat_jobs_show**](StatisticApi.md#stat_jobs_show) | **GET** /api/stat/jobs/{id} | Load job result |


# **stat_jobs_create**
> StatJobsCreate200Response stat_jobs_create(stat_jobs_create_request)

Create new job

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.stat_jobs_create200_response import StatJobsCreate200Response
from bsg_api.models.stat_jobs_create_request import StatJobsCreateRequest
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
    api_instance = bsg_api.StatisticApi(api_client)
    stat_jobs_create_request = bsg_api.StatJobsCreateRequest() # StatJobsCreateRequest | 

    try:
        # Create new job
        api_response = api_instance.stat_jobs_create(stat_jobs_create_request)
        print("The response of StatisticApi->stat_jobs_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatisticApi->stat_jobs_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **stat_jobs_create_request** | [**StatJobsCreateRequest**](StatJobsCreateRequest.md) |  |  |

### Return type

[**StatJobsCreate200Response**](StatJobsCreate200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stat_jobs_delete**
> StatJobsDelete200Response stat_jobs_delete(id)

Delete job result

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.stat_jobs_delete200_response import StatJobsDelete200Response
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
    api_instance = bsg_api.StatisticApi(api_client)
    id = '3941ffacdd698b404e' # str | Job identifier

    try:
        # Delete job result
        api_response = api_instance.stat_jobs_delete(id)
        print("The response of StatisticApi->stat_jobs_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatisticApi->stat_jobs_delete: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Job identifier |  |

### Return type

[**StatJobsDelete200Response**](StatJobsDelete200Response.md)

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

# **stat_jobs_list**
> object stat_jobs_list()

List statistic jobs

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
    api_instance = bsg_api.StatisticApi(api_client)

    try:
        # List statistic jobs
        api_response = api_instance.stat_jobs_list()
        print("The response of StatisticApi->stat_jobs_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatisticApi->stat_jobs_list: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stat_jobs_show**
> object stat_jobs_show(id)

Load job result

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
    api_instance = bsg_api.StatisticApi(api_client)
    id = '3941ffacdd698b404e' # str | Job identifier

    try:
        # Load job result
        api_response = api_instance.stat_jobs_show(id)
        print("The response of StatisticApi->stat_jobs_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatisticApi->stat_jobs_show: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | Job identifier |  |

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
| **200** | Successful operation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

