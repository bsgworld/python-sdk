# RcsStatusCallback

RCS status callback object

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **int** | error code, 0 - if successful | [optional]  |
| **error_description** | **str** | error description | [optional]  |
| **id** | **int** | Message ID – a unique identifier automatically generated on the Platform when the message is created | [optional]  |
| **msisdn** | **str** | Phone number without leading plus, just digits | [optional]  |
| **reference** | **str** | external unique ID. String up to 32 characters containing only alpha numeric characters.  **Please note:** messages with duplicate reference_id will be rejected | [optional]  |
| **time_in** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **time_sent** | **datetime** | Date and time of sending the message | [optional]  |
| **time_dr** | **datetime** | Date and time of receipt of the delivery report response | [optional]  |
| **status** | [**MessageStatus**](MessageStatus.md) |  | [optional]  |
| **price** | **float** | Message price | [optional]  |
| **currency** | **str** | The currency code of the account. Specified according to the ISO-4217 standard | [optional]  |

## Example

```python
from bsg_api.models.rcs_status_callback import RcsStatusCallback

# TODO update the JSON string below
json = "{}"
# create an instance of RcsStatusCallback from a JSON string
rcs_status_callback_instance = RcsStatusCallback.from_json(json)
# print the JSON string representation of the object
print(RcsStatusCallback.to_json())

# convert the object into a dict
rcs_status_callback_dict = rcs_status_callback_instance.to_dict()
# create an instance of RcsStatusCallback from a dict
rcs_status_callback_from_dict = RcsStatusCallback.from_dict(rcs_status_callback_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

