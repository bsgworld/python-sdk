# ShortUrlsLinkDelete422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | Short link not found. Please check short link id. | [optional]  |

## Example

```python
from bsg_api.models.short_urls_link_delete422_response import ShortUrlsLinkDelete422Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsLinkDelete422Response from a JSON string
short_urls_link_delete422_response_instance = ShortUrlsLinkDelete422Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsLinkDelete422Response.to_json())

# convert the object into a dict
short_urls_link_delete422_response_dict = short_urls_link_delete422_response_instance.to_dict()
# create an instance of ShortUrlsLinkDelete422Response from a dict
short_urls_link_delete422_response_from_dict = ShortUrlsLinkDelete422Response.from_dict(short_urls_link_delete422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

