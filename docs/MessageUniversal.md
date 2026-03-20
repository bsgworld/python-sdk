# MessageUniversal

A message that can be of type SMS, WhatsApp, or RCS.

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **channels** | **List[str]** |  |  |
| **phone** | [**Phone**](Phone.md) |  |  |
| **rcs** | [**Rcs**](Rcs.md) |  | [optional]  |
| **viber** | [**Viber**](Viber.md) |  | [optional]  |
| **sms** | [**Sms**](Sms.md) |  | [optional]  |
| **voice** | [**Voice**](Voice.md) |  | [optional]  |
| **telegram** | [**Telegram**](Telegram.md) |  | [optional]  |
| **callback_url** | **object** | Link to get the delivery status of messages. If this parameter is specified in the method, it will take precedence over the value specified in the “Callback URL” field in the Personal Area. | [optional]  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **validity_seconds** | **int** | Message validity period in seconds. After this period expires, the message will be in **EXPIRED** status or will be redirected to the SMS channel if it was specified in the request. Incompatible with **validity** | [optional]  |
| **respect_curfew** | **bool** | Check the curfew if it&#39;s set up in user settings. | [optional] [default to False] |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to True] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to True] |
| **dry_run** | **bool** | Allows you to check the validity of the request without actual message sending | [optional] [default to False] |

## Example

```python
from bsg_api.models.message_universal import MessageUniversal

# TODO update the JSON string below
json = "{}"
# create an instance of MessageUniversal from a JSON string
message_universal_instance = MessageUniversal.from_json(json)
# print the JSON string representation of the object
print(MessageUniversal.to_json())

# convert the object into a dict
message_universal_dict = message_universal_instance.to_dict()
# create an instance of MessageUniversal from a dict
message_universal_from_dict = MessageUniversal.from_dict(message_universal_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

