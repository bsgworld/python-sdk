# StoplistSearchMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**MetaPage**](MetaPage.md) |  | [optional]  |
| **search** | [**StoplistSearchCriteria**](StoplistSearchCriteria.md) |  | [optional]  |

## Example

```python
from bsg_api.models.stoplist_search_meta import StoplistSearchMeta

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistSearchMeta from a JSON string
stoplist_search_meta_instance = StoplistSearchMeta.from_json(json)
# print the JSON string representation of the object
print(StoplistSearchMeta.to_json())

# convert the object into a dict
stoplist_search_meta_dict = stoplist_search_meta_instance.to_dict()
# create an instance of StoplistSearchMeta from a dict
stoplist_search_meta_from_dict = StoplistSearchMeta.from_dict(stoplist_search_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

