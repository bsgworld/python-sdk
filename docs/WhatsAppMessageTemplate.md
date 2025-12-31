# WhatsAppMessageTemplate

Required for type \"template\"

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | Template name |  |
| **language** | [**Language**](Language.md) |  |  |
| **components** | [**List[Components]**](Components.md) |  |  |

## Example

```python
from bsg_api.models.whats_app_message_template import WhatsAppMessageTemplate

# TODO update the JSON string below
json = "{}"
# create an instance of WhatsAppMessageTemplate from a JSON string
whats_app_message_template_instance = WhatsAppMessageTemplate.from_json(json)
# print the JSON string representation of the object
print(WhatsAppMessageTemplate.to_json())

# convert the object into a dict
whats_app_message_template_dict = whats_app_message_template_instance.to_dict()
# create an instance of WhatsAppMessageTemplate from a dict
whats_app_message_template_from_dict = WhatsAppMessageTemplate.from_dict(whats_app_message_template_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

