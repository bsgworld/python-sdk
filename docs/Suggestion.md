# Suggestion

Object describe action when user click on button, it may be call to the phone or redirect to the link

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **str** | text of the button |  |
| **url** | **str** | A link to go through a click on the button. The link should start with http/https.  If you need to add a button to unsubscribe the user from the mailing list, you can specify a link in the format http://nosms.cc/XXXX – the Platform will generate an Unsubscribe link for this action when sending the message. When the user clicks on the unsubscribe button, the user’s number will be added to the RCS email stop list. |  |
| **postback_data** | **str** | Extra data to send on callback_url when user click on the button | [optional]  |
| **phone** | **str** | Phone number to call with a click of a button. 9 – 15 characters (the length must take into account the country code and phone number, the phone number is indicated without +). When sending RCS messages to the country of Ukraine, the phone number to call via the button must be a Ukrainian number |  |

## Example

```python
from bsg_api.models.suggestion import Suggestion

# TODO update the JSON string below
json = "{}"
# create an instance of Suggestion from a JSON string
suggestion_instance = Suggestion.from_json(json)
# print the JSON string representation of the object
print(Suggestion.to_json())

# convert the object into a dict
suggestion_dict = suggestion_instance.to_dict()
# create an instance of Suggestion from a dict
suggestion_from_dict = Suggestion.from_dict(suggestion_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

