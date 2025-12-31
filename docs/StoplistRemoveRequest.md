# StoplistRemoveRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ids** | **List[int]** | An array of contact IDs to remove from stop list |  |
| **types** | **List[str]** | Specify the stop list type from which you want to remove contacts |  |

## Example

```python
from bsg_api.models.stoplist_remove_request import StoplistRemoveRequest

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistRemoveRequest from a JSON string
stoplist_remove_request_instance = StoplistRemoveRequest.from_json(json)
# print the JSON string representation of the object
print(StoplistRemoveRequest.to_json())

# convert the object into a dict
stoplist_remove_request_dict = stoplist_remove_request_instance.to_dict()
# create an instance of StoplistRemoveRequest from a dict
stoplist_remove_request_from_dict = StoplistRemoveRequest.from_dict(stoplist_remove_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

