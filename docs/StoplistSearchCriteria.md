# StoplistSearchCriteria

Search criteria

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_field** | [**StoplistSearchField**](StoplistSearchField.md) |  | [optional]  |
| **operator** | [**SearchOperator**](SearchOperator.md) |  | [optional]  |
| **value** | **str** | Value to to find using search[field] and search[operator] | [optional]  |

## Example

```python
from bsg_api.models.stoplist_search_criteria import StoplistSearchCriteria

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistSearchCriteria from a JSON string
stoplist_search_criteria_instance = StoplistSearchCriteria.from_json(json)
# print the JSON string representation of the object
print(StoplistSearchCriteria.to_json())

# convert the object into a dict
stoplist_search_criteria_dict = stoplist_search_criteria_instance.to_dict()
# create an instance of StoplistSearchCriteria from a dict
stoplist_search_criteria_from_dict = StoplistSearchCriteria.from_dict(stoplist_search_criteria_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

