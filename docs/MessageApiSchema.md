# MessageApiSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Message ID – a unique identifier automatically generated on the Platform when the message is created | [optional]  |
| **campaign_id** | **int** | campaign unique identifier | [optional]  |
| **reference_id** | **str** | external unique ID. String up to 32 characters containing only alpha numeric characters.  **Please note:** messages with duplicate reference_id will be rejected | [optional]  |
| **type** | [**MessageType**](MessageType.md) |  | [optional]  |
| **source** | [**MessageSource**](MessageSource.md) |  | [optional]  |
| **text** | **str** | Message text to send | [optional]  |
| **phone** | **int** | Phone number without leading plus, just digits | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **status** | [**MessageStatus**](MessageStatus.md) |  | [optional]  |
| **amount** | [**MessagePriceObject**](MessagePriceObject.md) |  | [optional]  |
| **sender** | **str** | Sender name.   Up to 11 Latin letters or digits, up to 15 – only digits. To setup senders visit the [account](https://app.bsg.world/sms/senders) or use [sender api](#tag/Senders) | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **sent_at** | **datetime** | Date and time of sending the message | [optional]  |
| **delivered_at** | **datetime** | Date and time of receipt of the delivery report response | [optional]  |
| **country** | **str** | Country code according to ISO 3166-1 alpha-2 standard | [optional]  |
| **parts** | **int** |  | [optional]  |
| **rcs_options** | [**Options**](Options.md) |  | [optional]  |
| **alternative_channels** | [**MessageApiSchemaAlternativeChannels**](MessageApiSchemaAlternativeChannels.md) |  | [optional]  |

## Example

```python
from bsg_api.models.message_api_schema import MessageApiSchema

# TODO update the JSON string below
json = "{}"
# create an instance of MessageApiSchema from a JSON string
message_api_schema_instance = MessageApiSchema.from_json(json)
# print the JSON string representation of the object
print(MessageApiSchema.to_json())

# convert the object into a dict
message_api_schema_dict = message_api_schema_instance.to_dict()
# create an instance of MessageApiSchema from a dict
message_api_schema_from_dict = MessageApiSchema.from_dict(message_api_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

