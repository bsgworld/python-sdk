# GetMessages200ResponseMetaPage

Pagination parameters and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **int** | Total items count at all of the pages | [optional]  |
| **limit** | **int** | Limit items at one page | [optional]  |
| **offset** | **int** | Get items starting at offset | [optional] [default to 0] |

## Example

```python
from bsg_api.models.get_messages200_response_meta_page import GetMessages200ResponseMetaPage

# TODO update the JSON string below
json = "{}"
# create an instance of GetMessages200ResponseMetaPage from a JSON string
get_messages200_response_meta_page_instance = GetMessages200ResponseMetaPage.from_json(json)
# print the JSON string representation of the object
print(GetMessages200ResponseMetaPage.to_json())

# convert the object into a dict
get_messages200_response_meta_page_dict = get_messages200_response_meta_page_instance.to_dict()
# create an instance of GetMessages200ResponseMetaPage from a dict
get_messages200_response_meta_page_from_dict = GetMessages200ResponseMetaPage.from_dict(get_messages200_response_meta_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

