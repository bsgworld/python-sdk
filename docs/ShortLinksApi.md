# bsg_api.ShortLinksApi

All URIs are relative to *https://one-api.bsg.world*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**short_urls_clicks**](ShortLinksApi.md#short_urls_clicks) | **GET** /api/short-url/clicks | List of clicks |
| [**short_urls_link**](ShortLinksApi.md#short_urls_link) | **GET** /api/short-url/links/{uuid}/statistics | Get short link statistic |
| [**short_urls_link_create**](ShortLinksApi.md#short_urls_link_create) | **POST** /api/short-url/links | Create short link |
| [**short_urls_link_delete**](ShortLinksApi.md#short_urls_link_delete) | **DELETE** /api/short-url/links/{uuid} | Remove short link |
| [**short_urls_link_update**](ShortLinksApi.md#short_urls_link_update) | **PUT** /api/short-url/links/{uuid} | Update short link |
| [**short_urls_links**](ShortLinksApi.md#short_urls_links) | **GET** /api/short-url/links | List of short links |


# **short_urls_clicks**
> ShortUrlsClicks200Response short_urls_clicks(var_from, to, page=page, per_page=per_page, campaign=campaign)

List of clicks

List of all clicks for selected period *from* - *to* with pagination by *per_page*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_clicks200_response import ShortUrlsClicks200Response
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
    api_instance = bsg_api.ShortLinksApi(api_client)
    var_from = '2022-04-28' # str | From date
    to = '2022-04-28' # str | To date
    page = 1 # int | Get items starting from this page. (optional) (default to 1)
    per_page = 20 # int | The number of items in the page. Possible values are from 10 to 500. (optional) (default to 20)
    campaign = 56 # int | Campaign id to get only clicks on short link sent as part on [sms campaign](#tag/Campaign-SMS) (optional)

    try:
        # List of clicks
        api_response = api_instance.short_urls_clicks(var_from, to, page=page, per_page=per_page, campaign=campaign)
        print("The response of ShortLinksApi->short_urls_clicks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortLinksApi->short_urls_clicks: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_from** | **str** | From date |  |
| **to** | **str** | To date |  |
| **page** | **int** | Get items starting from this page. | [optional] [default to 1] |
| **per_page** | **int** | The number of items in the page. Possible values are from 10 to 500. | [optional] [default to 20] |
| **campaign** | **int** | Campaign id to get only clicks on short link sent as part on [sms campaign](#tag/Campaign-SMS) | [optional]  |

### Return type

[**ShortUrlsClicks200Response**](ShortUrlsClicks200Response.md)

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

# **short_urls_link**
> ShortUrlsLink200Response short_urls_link(uuid)

Get short link statistic

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_link200_response import ShortUrlsLink200Response
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
    api_instance = bsg_api.ShortLinksApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity

    try:
        # Get short link statistic
        api_response = api_instance.short_urls_link(uuid)
        print("The response of ShortLinksApi->short_urls_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortLinksApi->short_urls_link: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |

### Return type

[**ShortUrlsLink200Response**](ShortUrlsLink200Response.md)

### Authorization

[ExternalAuth](../README.md#ExternalAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
| ----------- | ----------- | ---------------- |
| **200** | Short link statistic |  -  |
| **404** | Short link not found. Pass correct link uuid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **short_urls_link_create**
> ShortUrlsLinkCreate201Response short_urls_link_create(link_store_request)

Create short link

Create a short link for original link.

**Please note:** *Response contains new link status. If original link is used at first time it may not pass the moderation automatically.
Be careful only link in **active** status can be used for redirect!*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.link_store_request import LinkStoreRequest
from bsg_api.models.short_urls_link_create201_response import ShortUrlsLinkCreate201Response
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
    api_instance = bsg_api.ShortLinksApi(api_client)
    link_store_request = bsg_api.LinkStoreRequest() # LinkStoreRequest | 

    try:
        # Create short link
        api_response = api_instance.short_urls_link_create(link_store_request)
        print("The response of ShortLinksApi->short_urls_link_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortLinksApi->short_urls_link_create: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **link_store_request** | [**LinkStoreRequest**](LinkStoreRequest.md) |  |  |

### Return type

[**ShortUrlsLinkCreate201Response**](ShortUrlsLinkCreate201Response.md)

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

# **short_urls_link_delete**
> object short_urls_link_delete(uuid)

Remove short link

If short link is *active* it will be *deleted*. Next few days this action can be reverted and link
may become *active* again. If short link already *blocked* or *deleted* it will be removed permanently. 


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
    api_instance = bsg_api.ShortLinksApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity

    try:
        # Remove short link
        api_response = api_instance.short_urls_link_delete(uuid)
        print("The response of ShortLinksApi->short_urls_link_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortLinksApi->short_urls_link_delete: %s\n" % e)
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
| **422** | Short link not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **short_urls_link_update**
> ShortUrlsLinkUpdate200Response short_urls_link_update(uuid, link_update_request)

Update short link

You can update short link name, slug or original link

**Please note:** If you change the original link to new one that hasn't been ever used before it may requires moderation
and short link status may be changed to *blocked*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.link_update_request import LinkUpdateRequest
from bsg_api.models.short_urls_link_update200_response import ShortUrlsLinkUpdate200Response
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
    api_instance = bsg_api.ShortLinksApi(api_client)
    uuid = 'uuid_example' # str | Uuid of entity
    link_update_request = {"name":"New name"} # LinkUpdateRequest | 

    try:
        # Update short link
        api_response = api_instance.short_urls_link_update(uuid, link_update_request)
        print("The response of ShortLinksApi->short_urls_link_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortLinksApi->short_urls_link_update: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **str** | Uuid of entity |  |
| **link_update_request** | [**LinkUpdateRequest**](LinkUpdateRequest.md) |  |  |

### Return type

[**ShortUrlsLinkUpdate200Response**](ShortUrlsLinkUpdate200Response.md)

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

# **short_urls_links**
> ShortUrlsLinks200Response short_urls_links(var_from, to, page=page, per_page=per_page)

List of short links

List of all created short links of selected period *from* to *to* with pagination by *per_page*

### Example

* Bearer (JWT) Authentication (ExternalAuth):

```python
import bsg_api
from bsg_api.models.short_urls_links200_response import ShortUrlsLinks200Response
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
    api_instance = bsg_api.ShortLinksApi(api_client)
    var_from = '2022-04-28' # str | From date
    to = '2022-04-28' # str | To date
    page = 1 # int | Get items starting from this page. (optional) (default to 1)
    per_page = 20 # int | The number of items in the page. Possible values are from 10 to 500. (optional) (default to 20)

    try:
        # List of short links
        api_response = api_instance.short_urls_links(var_from, to, page=page, per_page=per_page)
        print("The response of ShortLinksApi->short_urls_links:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ShortLinksApi->short_urls_links: %s\n" % e)
```



### Parameters


| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_from** | **str** | From date |  |
| **to** | **str** | To date |  |
| **page** | **int** | Get items starting from this page. | [optional] [default to 1] |
| **per_page** | **int** | The number of items in the page. Possible values are from 10 to 500. | [optional] [default to 20] |

### Return type

[**ShortUrlsLinks200Response**](ShortUrlsLinks200Response.md)

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

