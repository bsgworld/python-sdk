# StoplistSearch200ResponseMetaPage

Pagination parameters and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **int** | Total items count at all of the pages | [optional]  |
| **limit** | **int** | Limit items at one page | [optional]  |
| **offset** | **int** | Get items starting at offset | [optional] [default to 0] |

## Example

```python
from bsg_api.models.stoplist_search200_response_meta_page import StoplistSearch200ResponseMetaPage

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistSearch200ResponseMetaPage from a JSON string
stoplist_search200_response_meta_page_instance = StoplistSearch200ResponseMetaPage.from_json(json)
# print the JSON string representation of the object
print(StoplistSearch200ResponseMetaPage.to_json())

# convert the object into a dict
stoplist_search200_response_meta_page_dict = stoplist_search200_response_meta_page_instance.to_dict()
# create an instance of StoplistSearch200ResponseMetaPage from a dict
stoplist_search200_response_meta_page_from_dict = StoplistSearch200ResponseMetaPage.from_dict(stoplist_search200_response_meta_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

