# StoplistAddRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phones** | **List[int]** | Array of the phone numbers |  |
| **types** | **List[str]** | Specify the stop list type |  |

## Example

```python
from bsg_api.models.stoplist_add_request import StoplistAddRequest

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistAddRequest from a JSON string
stoplist_add_request_instance = StoplistAddRequest.from_json(json)
# print the JSON string representation of the object
print(StoplistAddRequest.to_json())

# convert the object into a dict
stoplist_add_request_dict = stoplist_add_request_instance.to_dict()
# create an instance of StoplistAddRequest from a dict
stoplist_add_request_from_dict = StoplistAddRequest.from_dict(stoplist_add_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

