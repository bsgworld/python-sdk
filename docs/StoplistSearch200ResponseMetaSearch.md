# StoplistSearch200ResponseMetaSearch

Search criteria

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_field** | [**StoplistSearchField**](StoplistSearchField.md) |  | [optional]  |
| **operator** | [**SearchOperator**](SearchOperator.md) |  | [optional]  |
| **value** | **str** | Value to to find using search[field] and search[operator] | [optional]  |

## Example

```python
from bsg_api.models.stoplist_search200_response_meta_search import StoplistSearch200ResponseMetaSearch

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistSearch200ResponseMetaSearch from a JSON string
stoplist_search200_response_meta_search_instance = StoplistSearch200ResponseMetaSearch.from_json(json)
# print the JSON string representation of the object
print(StoplistSearch200ResponseMetaSearch.to_json())

# convert the object into a dict
stoplist_search200_response_meta_search_dict = stoplist_search200_response_meta_search_instance.to_dict()
# create an instance of StoplistSearch200ResponseMetaSearch from a dict
stoplist_search200_response_meta_search_from_dict = StoplistSearch200ResponseMetaSearch.from_dict(stoplist_search200_response_meta_search_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

