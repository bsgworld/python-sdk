# Card

Either \"media\" or \"text\" is required.

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **str** | Message title | [optional]  |
| **text** | **str** | It is specified only for the “text” message type. RCS message text is up to 1000 characters. Can contain emojis (character count for emojis according to UTF-16 code points. Simple emojis take 2 code points, complex emojis take 4, Cyrillic emojis take 1). If the message contains a link in the format http://nosms.cc/XXXX, the System will generate an Unsubscribe link while sending the message  **Please note:** If the message contains a media object, the text parameter is optional and can be omitted | [optional]  |
| **media** | [**Media**](Media.md) |  | [optional]  |
| **suggestions** | [**List[Suggestion]**](Suggestion.md) | An array of objects containing information about nested buttons. Only up to 2 buttons can be added to a card. | [optional]  |

## Example

```python
from bsg_api.models.card import Card

# TODO update the JSON string below
json = "{}"
# create an instance of Card from a JSON string
card_instance = Card.from_json(json)
# print the JSON string representation of the object
print(Card.to_json())

# convert the object into a dict
card_dict = card_instance.to_dict()
# create an instance of Card from a dict
card_from_dict = Card.from_dict(card_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

