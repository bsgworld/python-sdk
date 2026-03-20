# MessageApiSchemaAlternativeChannelsSmsDetails


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parts** | **int** |  | [optional]  |
| **id** | **List[int]** |  | [optional]  |

## Example

```python
from bsg_api.models.message_api_schema_alternative_channels_sms_details import MessageApiSchemaAlternativeChannelsSmsDetails

# TODO update the JSON string below
json = "{}"
# create an instance of MessageApiSchemaAlternativeChannelsSmsDetails from a JSON string
message_api_schema_alternative_channels_sms_details_instance = MessageApiSchemaAlternativeChannelsSmsDetails.from_json(json)
# print the JSON string representation of the object
print(MessageApiSchemaAlternativeChannelsSmsDetails.to_json())

# convert the object into a dict
message_api_schema_alternative_channels_sms_details_dict = message_api_schema_alternative_channels_sms_details_instance.to_dict()
# create an instance of MessageApiSchemaAlternativeChannelsSmsDetails from a dict
message_api_schema_alternative_channels_sms_details_from_dict = MessageApiSchemaAlternativeChannelsSmsDetails.from_dict(message_api_schema_alternative_channels_sms_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

