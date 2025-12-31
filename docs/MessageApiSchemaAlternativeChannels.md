# MessageApiSchemaAlternativeChannels


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sms** | [**MessageApiSchemaAlternativeChannelsOneOf0Sms**](MessageApiSchemaAlternativeChannelsOneOf0Sms.md) |  | [optional]  |
| **viber** | [**MessageApiSchemaAlternativeChannelsOneOf1Viber**](MessageApiSchemaAlternativeChannelsOneOf1Viber.md) |  | [optional]  |

## Example

```python
from bsg_api.models.message_api_schema_alternative_channels import MessageApiSchemaAlternativeChannels

# TODO update the JSON string below
json = "{}"
# create an instance of MessageApiSchemaAlternativeChannels from a JSON string
message_api_schema_alternative_channels_instance = MessageApiSchemaAlternativeChannels.from_json(json)
# print the JSON string representation of the object
print(MessageApiSchemaAlternativeChannels.to_json())

# convert the object into a dict
message_api_schema_alternative_channels_dict = message_api_schema_alternative_channels_instance.to_dict()
# create an instance of MessageApiSchemaAlternativeChannels from a dict
message_api_schema_alternative_channels_from_dict = MessageApiSchemaAlternativeChannels.from_dict(message_api_schema_alternative_channels_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

