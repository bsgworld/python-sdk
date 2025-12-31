# Sms

The object contains information about the message for alternative delivery via SMS

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **str** | SMS text, max length is 765 chars for GSM 7-bit encoding (Latin), and 355 for UCS-2 |  |
| **sender** | **str** | Sender name.   Up to 11 Latin letters or digits, up to 15 – only digits. To setup senders visit the [account](https://app.bsg.world/sms/senders) or use [sender api](#tag/Senders) |  |
| **validity_seconds** | **int** | Validity period in seconds. If not set, validity field is used | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **check_stop_list** | **bool** |  | [optional] [default to True] |

## Example

```python
from bsg_api.models.sms import Sms

# TODO update the JSON string below
json = "{}"
# create an instance of Sms from a JSON string
sms_instance = Sms.from_json(json)
# print the JSON string representation of the object
print(Sms.to_json())

# convert the object into a dict
sms_dict = sms_instance.to_dict()
# create an instance of Sms from a dict
sms_from_dict = Sms.from_dict(sms_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

