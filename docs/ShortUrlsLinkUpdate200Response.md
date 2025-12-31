# ShortUrlsLinkUpdate200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**ShortUrlLinkSchema**](ShortUrlLinkSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.short_urls_link_update200_response import ShortUrlsLinkUpdate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsLinkUpdate200Response from a JSON string
short_urls_link_update200_response_instance = ShortUrlsLinkUpdate200Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsLinkUpdate200Response.to_json())

# convert the object into a dict
short_urls_link_update200_response_dict = short_urls_link_update200_response_instance.to_dict()
# create an instance of ShortUrlsLinkUpdate200Response from a dict
short_urls_link_update200_response_from_dict = ShortUrlsLinkUpdate200Response.from_dict(short_urls_link_update200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

