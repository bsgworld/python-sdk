# SmsSendRequestPhonesItem


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **number** | **int** | Phone number without leading plus, just digits |  |
| **reference_id** | **str** | external unique ID. String up to 32 characters containing only alpha numeric characters.  **Please note:** messages with duplicate reference_id will be rejected | [optional]  |

## Example

```python
from bsg_api.models.sms_send_request_phones_item import SmsSendRequestPhonesItem

# TODO update the JSON string below
json = "{}"
# create an instance of SmsSendRequestPhonesItem from a JSON string
sms_send_request_phones_item_instance = SmsSendRequestPhonesItem.from_json(json)
# print the JSON string representation of the object
print(SmsSendRequestPhonesItem.to_json())

# convert the object into a dict
sms_send_request_phones_item_dict = sms_send_request_phones_item_instance.to_dict()
# create an instance of SmsSendRequestPhonesItem from a dict
sms_send_request_phones_item_from_dict = SmsSendRequestPhonesItem.from_dict(sms_send_request_phones_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

