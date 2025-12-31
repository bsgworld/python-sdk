# WhatsAppMessage


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | [**Phone**](Phone.md) |  |  |
| **sender** | **str** |  |  |
| **type** | **str** |  |  |
| **template** | [**WhatsAppMessageTemplate**](WhatsAppMessageTemplate.md) |  | [optional]  |
| **alternative_channel** | [**WhatsAppMessageAlternativeChannel**](WhatsAppMessageAlternativeChannel.md) |  | [optional]  |
| **callback_url** | **object** | Link to get the delivery status of messages. If this parameter is specified in the method, it will take precedence over the value specified in the “Callback URL” field in the Personal Area. | [optional]  |
| **add_to_contact_book** | **bool** |  | [optional] [default to True] |
| **check_stop_list** | **bool** |  | [optional] [default to True] |

## Example

```python
from bsg_api.models.whats_app_message import WhatsAppMessage

# TODO update the JSON string below
json = "{}"
# create an instance of WhatsAppMessage from a JSON string
whats_app_message_instance = WhatsAppMessage.from_json(json)
# print the JSON string representation of the object
print(WhatsAppMessage.to_json())

# convert the object into a dict
whats_app_message_dict = whats_app_message_instance.to_dict()
# create an instance of WhatsAppMessage from a dict
whats_app_message_from_dict = WhatsAppMessage.from_dict(whats_app_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

