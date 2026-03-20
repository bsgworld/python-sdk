# Rcs


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cards** | [**List[Card]**](Card.md) | The array contains information about the card. The maximum number of cards is 5. Messages with one card are called “Single card”, messages with 2 or more cards are called “Carousel”. Depending on the chosen tariff, the number of cards may be limited (for example, you can send only Single cards).  Details will be provided by manager. |  |
| **text** | **str** | It is specified only for the “text” message type. RCS message text is  up to 160 characters. Can contain emojis (character count for emojis according to UTF-16 code points. Simple emojis take 2 code points, complex emojis take 4, Cyrillic emojis take 1). If the message contains a link in the format http://nosms.cc/XXXX, the System will generate an Unsubscribe link while sending the message |  |
| **sender** | **str** | The name of the agent used to send the rcs message |  |

## Example

```python
from bsg_api.models.rcs import Rcs

# TODO update the JSON string below
json = "{}"
# create an instance of Rcs from a JSON string
rcs_instance = Rcs.from_json(json)
# print the JSON string representation of the object
print(Rcs.to_json())

# convert the object into a dict
rcs_dict = rcs_instance.to_dict()
# create an instance of Rcs from a dict
rcs_from_dict = Rcs.from_dict(rcs_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

