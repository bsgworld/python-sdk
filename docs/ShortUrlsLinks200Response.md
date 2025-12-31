# ShortUrlsLinks200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ShortUrlLinkSchema]**](ShortUrlLinkSchema.md) |  | [optional]  |
| **total** | **int** | The total number of items matching the specified criteria | [optional]  |

## Example

```python
from bsg_api.models.short_urls_links200_response import ShortUrlsLinks200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsLinks200Response from a JSON string
short_urls_links200_response_instance = ShortUrlsLinks200Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsLinks200Response.to_json())

# convert the object into a dict
short_urls_links200_response_dict = short_urls_links200_response_instance.to_dict()
# create an instance of ShortUrlsLinks200Response from a dict
short_urls_links200_response_from_dict = ShortUrlsLinks200Response.from_dict(short_urls_links200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

