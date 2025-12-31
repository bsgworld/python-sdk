# ShortUrlsLinkUpdate422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | It may be one of the following:   - **The short link already exists** This error can occur when passed slug already used by another short link on this domain. Please try another slug. - **Short link not found** This error can occur when passed link id doesn&#39;t exist. Please check short link id.  | [optional]  |

## Example

```python
from bsg_api.models.short_urls_link_update422_response import ShortUrlsLinkUpdate422Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsLinkUpdate422Response from a JSON string
short_urls_link_update422_response_instance = ShortUrlsLinkUpdate422Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsLinkUpdate422Response.to_json())

# convert the object into a dict
short_urls_link_update422_response_dict = short_urls_link_update422_response_instance.to_dict()
# create an instance of ShortUrlsLinkUpdate422Response from a dict
short_urls_link_update422_response_from_dict = ShortUrlsLinkUpdate422Response.from_dict(short_urls_link_update422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

