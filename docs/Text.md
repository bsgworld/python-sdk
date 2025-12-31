# Text


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **str** | It is specified only for the “text” message type. RCS message text is  up to 160 characters. Can contain emojis (character count for emojis according to UTF-16 code points. Simple emojis take 2 code points, complex emojis take 4, Cyrillic emojis take 1). If the message contains a link in the format http://nosms.cc/XXXX, the System will generate an Unsubscribe link while sending the message |  |

## Example

```python
from bsg_api.models.text import Text

# TODO update the JSON string below
json = "{}"
# create an instance of Text from a JSON string
text_instance = Text.from_json(json)
# print the JSON string representation of the object
print(Text.to_json())

# convert the object into a dict
text_dict = text_instance.to_dict()
# create an instance of Text from a dict
text_from_dict = Text.from_dict(text_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

