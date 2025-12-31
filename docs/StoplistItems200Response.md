# StoplistItems200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[StopListPaginateSchema]**](StopListPaginateSchema.md) |  | [optional]  |
| **total** | **int** | Total items count at all of the pages | [optional]  |

## Example

```python
from bsg_api.models.stoplist_items200_response import StoplistItems200Response

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistItems200Response from a JSON string
stoplist_items200_response_instance = StoplistItems200Response.from_json(json)
# print the JSON string representation of the object
print(StoplistItems200Response.to_json())

# convert the object into a dict
stoplist_items200_response_dict = stoplist_items200_response_instance.to_dict()
# create an instance of StoplistItems200Response from a dict
stoplist_items200_response_from_dict = StoplistItems200Response.from_dict(stoplist_items200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

