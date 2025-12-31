# StopListCollection


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  | [optional]  |
| **phone** | **int** |  | [optional]  |
| **created_at** | **datetime** |  | [optional]  |
| **sms_stoplist** | **bool** |  | [optional] [default to True] |
| **viber_stoplist** | **bool** |  | [optional] [default to True] |
| **rcs_stoplist** | **bool** |  | [optional] [default to True] |

## Example

```python
from bsg_api.models.stop_list_collection import StopListCollection

# TODO update the JSON string below
json = "{}"
# create an instance of StopListCollection from a JSON string
stop_list_collection_instance = StopListCollection.from_json(json)
# print the JSON string representation of the object
print(StopListCollection.to_json())

# convert the object into a dict
stop_list_collection_dict = stop_list_collection_instance.to_dict()
# create an instance of StopListCollection from a dict
stop_list_collection_from_dict = StopListCollection.from_dict(stop_list_collection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

