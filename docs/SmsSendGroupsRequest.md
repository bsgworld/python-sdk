# SmsSendGroupsRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **groups** | **List[int]** | one or several contact list id to send messages. id of the lists can be obtained: using the Get [lists API](#tag/Contact-List) in your account [Contact Book → Lists](https://app.bsg.world/addressbook/lists) | [optional]  |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) |  |
| **text** | **str** | SMS text, max length is 765 chars for GSM 7-bit encoding (Latin), and 355 for UCS-2 |  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **short_links** | [**List[ShortLink]**](ShortLink.md) |  | [optional]  |
| **transliterate** | **bool** | apply transliteration to sms text if it necessary | [optional] [default to False] |

## Example

```python
from bsg_api.models.sms_send_groups_request import SmsSendGroupsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SmsSendGroupsRequest from a JSON string
sms_send_groups_request_instance = SmsSendGroupsRequest.from_json(json)
# print the JSON string representation of the object
print(SmsSendGroupsRequest.to_json())

# convert the object into a dict
sms_send_groups_request_dict = sms_send_groups_request_instance.to_dict()
# create an instance of SmsSendGroupsRequest from a dict
sms_send_groups_request_from_dict = SmsSendGroupsRequest.from_dict(sms_send_groups_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

