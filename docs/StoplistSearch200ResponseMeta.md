# StoplistSearch200ResponseMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**StoplistSearch200ResponseMetaPage**](StoplistSearch200ResponseMetaPage.md) |  | [optional]  |
| **search** | [**StoplistSearch200ResponseMetaSearch**](StoplistSearch200ResponseMetaSearch.md) |  | [optional]  |

## Example

```python
from bsg_api.models.stoplist_search200_response_meta import StoplistSearch200ResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistSearch200ResponseMeta from a JSON string
stoplist_search200_response_meta_instance = StoplistSearch200ResponseMeta.from_json(json)
# print the JSON string representation of the object
print(StoplistSearch200ResponseMeta.to_json())

# convert the object into a dict
stoplist_search200_response_meta_dict = stoplist_search200_response_meta_instance.to_dict()
# create an instance of StoplistSearch200ResponseMeta from a dict
stoplist_search200_response_meta_from_dict = StoplistSearch200ResponseMeta.from_dict(stoplist_search200_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

