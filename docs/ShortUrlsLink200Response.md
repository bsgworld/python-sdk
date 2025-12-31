# ShortUrlsLink200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**ShortUrlsLink200ResponseData**](ShortUrlsLink200ResponseData.md) |  | [optional]  |

## Example

```python
from bsg_api.models.short_urls_link200_response import ShortUrlsLink200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsLink200Response from a JSON string
short_urls_link200_response_instance = ShortUrlsLink200Response.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsLink200Response.to_json())

# convert the object into a dict
short_urls_link200_response_dict = short_urls_link200_response_instance.to_dict()
# create an instance of ShortUrlsLink200Response from a dict
short_urls_link200_response_from_dict = ShortUrlsLink200Response.from_dict(short_urls_link200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

