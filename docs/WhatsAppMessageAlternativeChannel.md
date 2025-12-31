# WhatsAppMessageAlternativeChannel


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sms** | [**Sms**](Sms.md) |  | [optional]  |

## Example

```python
from bsg_api.models.whats_app_message_alternative_channel import WhatsAppMessageAlternativeChannel

# TODO update the JSON string below
json = "{}"
# create an instance of WhatsAppMessageAlternativeChannel from a JSON string
whats_app_message_alternative_channel_instance = WhatsAppMessageAlternativeChannel.from_json(json)
# print the JSON string representation of the object
print(WhatsAppMessageAlternativeChannel.to_json())

# convert the object into a dict
whats_app_message_alternative_channel_dict = whats_app_message_alternative_channel_instance.to_dict()
# create an instance of WhatsAppMessageAlternativeChannel from a dict
whats_app_message_alternative_channel_from_dict = WhatsAppMessageAlternativeChannel.from_dict(whats_app_message_alternative_channel_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

