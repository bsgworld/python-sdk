# MetaPage

Pagination parameters and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **int** | Total items count at all of the pages | [optional]  |
| **limit** | **int** | Limit items at one page | [optional]  |
| **offset** | **int** | Get items starting at offset | [optional] [default to 0] |

## Example

```python
from bsg_api.models.meta_page import MetaPage

# TODO update the JSON string below
json = "{}"
# create an instance of MetaPage from a JSON string
meta_page_instance = MetaPage.from_json(json)
# print the JSON string representation of the object
print(MetaPage.to_json())

# convert the object into a dict
meta_page_dict = meta_page_instance.to_dict()
# create an instance of MetaPage from a dict
meta_page_from_dict = MetaPage.from_dict(meta_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

