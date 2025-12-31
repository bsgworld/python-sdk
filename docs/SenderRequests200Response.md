# SenderRequests200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[SenderRequestSchema]**](SenderRequestSchema.md) |  | [optional]  |
| **meta** | [**SenderRequests200ResponseMeta**](SenderRequests200ResponseMeta.md) |  | [optional]  |

## Example

```python
from bsg_api.models.sender_requests200_response import SenderRequests200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SenderRequests200Response from a JSON string
sender_requests200_response_instance = SenderRequests200Response.from_json(json)
# print the JSON string representation of the object
print(SenderRequests200Response.to_json())

# convert the object into a dict
sender_requests200_response_dict = sender_requests200_response_instance.to_dict()
# create an instance of SenderRequests200Response from a dict
sender_requests200_response_from_dict = SenderRequests200Response.from_dict(sender_requests200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

