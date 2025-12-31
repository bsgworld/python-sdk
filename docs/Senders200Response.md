# Senders200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[SenderSchema]**](SenderSchema.md) |  | [optional]  |
| **total** | **int** | Total items count at all of the pages | [optional]  |

## Example

```python
from bsg_api.models.senders200_response import Senders200Response

# TODO update the JSON string below
json = "{}"
# create an instance of Senders200Response from a JSON string
senders200_response_instance = Senders200Response.from_json(json)
# print the JSON string representation of the object
print(Senders200Response.to_json())

# convert the object into a dict
senders200_response_dict = senders200_response_instance.to_dict()
# create an instance of Senders200Response from a dict
senders200_response_from_dict = Senders200Response.from_dict(senders200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

