# Sms


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) |  |
| **text** | **str** | SMS text, max length is 765 chars for GSM 7-bit encoding (Latin), and 355 for UCS-2 |  |
| **unsubscribe_caption** | **str** | Caption before unsubscribe link. Space between caption and link is required. | [optional]  |
| **transliterate** | **bool** | apply transliteration to sms text if it necessary | [optional] [default to False] |
| **short_links** | [**List[ShortLink]**](ShortLink.md) | $shortLinks | [optional]  |

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

