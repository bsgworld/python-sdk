# ShortUrlsDomainCreate201Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**ShortUrlDomainSchema**](ShortUrlDomainSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.short_urls_domain_create201_response import ShortUrlsDomainCreate201Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsDomainCreate201Response from a JSON string
short_urls_domain_create201_response_instance = ShortUrlsDomainCreate201Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsDomainCreate201Response.to_json())

# convert the object into a dict
short_urls_domain_create201_response_dict = short_urls_domain_create201_response_instance.to_dict()
# create an instance of ShortUrlsDomainCreate201Response from a dict
short_urls_domain_create201_response_from_dict = ShortUrlsDomainCreate201Response.from_dict(short_urls_domain_create201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

