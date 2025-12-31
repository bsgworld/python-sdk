# ShortUrlsClicks200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ClickResource]**](ClickResource.md) |  | [optional]  |
| **total** | **int** | The total number of items matching the specified criteria | [optional]  |

## Example

```python
from bsg_api.models.short_urls_clicks200_response import ShortUrlsClicks200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsClicks200Response from a JSON string
short_urls_clicks200_response_instance = ShortUrlsClicks200Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsClicks200Response.to_json())

# convert the object into a dict
short_urls_clicks200_response_dict = short_urls_clicks200_response_instance.to_dict()
# create an instance of ShortUrlsClicks200Response from a dict
short_urls_clicks200_response_from_dict = ShortUrlsClicks200Response.from_dict(short_urls_clicks200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

