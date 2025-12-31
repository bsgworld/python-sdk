# MessageInfo


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Message ID – a unique identifier automatically generated on the Platform when the message is created | [optional]  |
| **reference_id** | **str** | external unique ID. String up to 32 characters containing only alpha numeric characters.  **Please note:** messages with duplicate reference_id will be rejected | [optional]  |
| **source** | [**MessageSource**](MessageSource.md) |  | [optional]  |
| **type** | [**MessageType**](MessageType.md) |  | [optional]  |
| **phone** | **int** | Phone number without leading plus, just digits | [optional]  |
| **status** | [**MessageStatus**](MessageStatus.md) |  | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **amount** | [**MessagePriceObject**](MessagePriceObject.md) |  | [optional]  |
| **sender** | **str** | Sender name.   Up to 11 Latin letters or digits, up to 15 – only digits. To setup senders visit the [account](https://app.bsg.world/sms/senders) or use [sender api](#tag/Senders) | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **sent_at** | **datetime** | Date and time of sending the message | [optional]  |
| **delivered_at** | **datetime** | Date and time of receipt of the delivery report response | [optional]  |

## Example

```python
from bsg_api.models.message_info import MessageInfo

# TODO update the JSON string below
json = "{}"
# create an instance of MessageInfo from a JSON string
message_info_instance = MessageInfo.from_json(json)
# print the JSON string representation of the object
print(MessageInfo.to_json())

# convert the object into a dict
message_info_dict = message_info_instance.to_dict()
# create an instance of MessageInfo from a dict
message_info_from_dict = MessageInfo.from_dict(message_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

