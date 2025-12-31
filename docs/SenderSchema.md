# SenderSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  | [optional]  |
| **status** | **str** |  | [optional]  |
| **country** | **str** | Country code according to ISO 3166-1 alpha-2 standard | [optional]  |
| **sender** | **str** | Sender name.   Up to 11 Latin letters or digits, up to 15 – only digits. To setup senders visit the [account](https://app.bsg.world/sms/senders) or use [sender api](#tag/Senders) | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **is_default** | **bool** |  | [optional]  |

## Example

```python
from bsg_api.models.sender_schema import SenderSchema

# TODO update the JSON string below
json = "{}"
# create an instance of SenderSchema from a JSON string
sender_schema_instance = SenderSchema.from_json(json)
# print the JSON string representation of the object
print(SenderSchema.to_json())

# convert the object into a dict
sender_schema_dict = sender_schema_instance.to_dict()
# create an instance of SenderSchema from a dict
sender_schema_from_dict = SenderSchema.from_dict(sender_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

