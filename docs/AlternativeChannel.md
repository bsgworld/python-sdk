# AlternativeChannel

The object contains information for sending a message via an alternative SMS channel in case of non-delivery with primary channel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sms** | [**Sms**](Sms.md) |  | [optional]  |

## Example

```python
from bsg_api.models.alternative_channel import AlternativeChannel

# TODO update the JSON string below
json = "{}"
# create an instance of AlternativeChannel from a JSON string
alternative_channel_instance = AlternativeChannel.from_json(json)
# print the JSON string representation of the object
print(AlternativeChannel.to_json())

# convert the object into a dict
alternative_channel_dict = alternative_channel_instance.to_dict()
# create an instance of AlternativeChannel from a dict
alternative_channel_from_dict = AlternativeChannel.from_dict(alternative_channel_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

