# Telegram

Currently telegram can be used only for OTP messages.

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sender** | **str** |  | [optional]  |
| **text** | **str** |  |  |

## Example

```python
from bsg_api.models.telegram import Telegram

# TODO update the JSON string below
json = "{}"
# create an instance of Telegram from a JSON string
telegram_instance = Telegram.from_json(json)
# print the JSON string representation of the object
print(Telegram.to_json())

# convert the object into a dict
telegram_dict = telegram_instance.to_dict()
# create an instance of Telegram from a dict
telegram_from_dict = Telegram.from_dict(telegram_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

