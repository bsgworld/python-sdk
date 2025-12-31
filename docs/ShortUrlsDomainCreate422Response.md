# ShortUrlsDomainCreate422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | It may be one of the following:  - **short-link.exceptions.domain_exceeded_allowed_limit** - Maximum allowed domain count already reached. Please delete unused domains or upgrade tariff - **Invalid domain name** - Duplicate domain name. This domain already exists use another domain name.  | [optional]  |

## Example

```python
from bsg_api.models.short_urls_domain_create422_response import ShortUrlsDomainCreate422Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsDomainCreate422Response from a JSON string
short_urls_domain_create422_response_instance = ShortUrlsDomainCreate422Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsDomainCreate422Response.to_json())

# convert the object into a dict
short_urls_domain_create422_response_dict = short_urls_domain_create422_response_instance.to_dict()
# create an instance of ShortUrlsDomainCreate422Response from a dict
short_urls_domain_create422_response_from_dict = ShortUrlsDomainCreate422Response.from_dict(short_urls_domain_create422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

