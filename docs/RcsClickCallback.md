# RcsClickCallback

RCS click callback object

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Message ID – a unique identifier automatically generated on the Platform when the message is created | [optional]  |
| **reference** | **str** | external unique ID. String up to 32 characters containing only alpha numeric characters.  **Please note:** messages with duplicate reference_id will be rejected | [optional]  |
| **msisdn** | **str** | Phone number without leading plus, just digits | [optional]  |
| **text** | **str** | Text on clicked button from suggestions | [optional]  |
| **postback** | **str** | postback_data field value from suggestion button object | [optional]  |
| **time_click** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |

## Example

```python
from bsg_api.models.rcs_click_callback import RcsClickCallback

# TODO update the JSON string below
json = "{}"
# create an instance of RcsClickCallback from a JSON string
rcs_click_callback_instance = RcsClickCallback.from_json(json)
# print the JSON string representation of the object
print(RcsClickCallback.to_json())

# convert the object into a dict
rcs_click_callback_dict = rcs_click_callback_instance.to_dict()
# create an instance of RcsClickCallback from a dict
rcs_click_callback_from_dict = RcsClickCallback.from_dict(rcs_click_callback_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

