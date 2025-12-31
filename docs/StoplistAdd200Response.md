# StoplistAdd200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[StopListCollection]**](StopListCollection.md) |  | [optional]  |

## Example

```python
from bsg_api.models.stoplist_add200_response import StoplistAdd200Response

# TODO update the JSON string below
json = "{}"
# create an instance of StoplistAdd200Response from a JSON string
stoplist_add200_response_instance = StoplistAdd200Response.from_json(json)
# print the JSON string representation of the object
print(StoplistAdd200Response.to_json())

# convert the object into a dict
stoplist_add200_response_dict = stoplist_add200_response_instance.to_dict()
# create an instance of StoplistAdd200Response from a dict
stoplist_add200_response_from_dict = StoplistAdd200Response.from_dict(stoplist_add200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

