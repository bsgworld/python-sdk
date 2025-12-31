# SenderRequests200ResponseMeta


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**SenderRequests200ResponseMetaPage**](SenderRequests200ResponseMetaPage.md) |  | [optional]  |

## Example

```python
from bsg_api.models.sender_requests200_response_meta import SenderRequests200ResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of SenderRequests200ResponseMeta from a JSON string
sender_requests200_response_meta_instance = SenderRequests200ResponseMeta.from_json(json)
# print the JSON string representation of the object
print(SenderRequests200ResponseMeta.to_json())

# convert the object into a dict
sender_requests200_response_meta_dict = sender_requests200_response_meta_instance.to_dict()
# create an instance of SenderRequests200ResponseMeta from a dict
sender_requests200_response_meta_from_dict = SenderRequests200ResponseMeta.from_dict(sender_requests200_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

