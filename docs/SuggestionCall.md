# SuggestionCall

Call when click the button

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **str** | text of the button |  |
| **phone** | **str** | Phone number to call with a click of a button. 9 – 15 characters (the length must take into account the country code and phone number, the phone number is indicated without +). When sending RCS messages to the country of Ukraine, the phone number to call via the button must be a Ukrainian number |  |
| **postback_data** | **str** | Extra data to send on callback_url when user click on the button | [optional]  |

## Example

```python
from bsg_api.models.suggestion_call import SuggestionCall

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestionCall from a JSON string
suggestion_call_instance = SuggestionCall.from_json(json)
# print the JSON string representation of the object
print(SuggestionCall.to_json())

# convert the object into a dict
suggestion_call_dict = suggestion_call_instance.to_dict()
# create an instance of SuggestionCall from a dict
suggestion_call_from_dict = SuggestionCall.from_dict(suggestion_call_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

