# SenderRequestLegal201Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**SenderRequestLegalSchema**](SenderRequestLegalSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.sender_request_legal201_response import SenderRequestLegal201Response

# TODO update the JSON string below
json = "{}"
# create an instance of SenderRequestLegal201Response from a JSON string
sender_request_legal201_response_instance = SenderRequestLegal201Response.from_json(json)
# print the JSON string representation of the object
print(SenderRequestLegal201Response.to_json())

# convert the object into a dict
sender_request_legal201_response_dict = sender_request_legal201_response_instance.to_dict()
# create an instance of SenderRequestLegal201Response from a dict
sender_request_legal201_response_from_dict = SenderRequestLegal201Response.from_dict(sender_request_legal201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

