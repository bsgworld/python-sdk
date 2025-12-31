# IndividualMessageData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | **int** | Phone number without leading plus, just digits |  |
| **text** | **str** | SMS text, max length is 765 chars for GSM 7-bit encoding (Latin), and 355 for UCS-2 |  |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) |  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **reference_id** | **str** | external unique ID. String up to 32 characters containing only alpha numeric characters.  **Please note:** messages with duplicate reference_id will be rejected | [optional]  |
| **transliterate** | **bool** | apply transliteration to sms text if it necessary | [optional] [default to False] |

## Example

```python
from bsg_api.models.individual_message_data import IndividualMessageData

# TODO update the JSON string below
json = "{}"
# create an instance of IndividualMessageData from a JSON string
individual_message_data_instance = IndividualMessageData.from_json(json)
# print the JSON string representation of the object
print(IndividualMessageData.to_json())

# convert the object into a dict
individual_message_data_dict = individual_message_data_instance.to_dict()
# create an instance of IndividualMessageData from a dict
individual_message_data_from_dict = IndividualMessageData.from_dict(individual_message_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

