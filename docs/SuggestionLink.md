# SuggestionLink

Redirect user to url link when click the button

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **text** | **str** | text of the button |  |
| **url** | **str** | A link to go through a click on the button. The link should start with http/https.  If you need to add a button to unsubscribe the user from the mailing list, you can specify a link in the format http://nosms.cc/XXXX – the Platform will generate an Unsubscribe link for this action when sending the message. When the user clicks on the unsubscribe button, the user’s number will be added to the RCS email stop list. |  |
| **postback_data** | **str** | Extra data to send on callback_url when user click on the button | [optional]  |

## Example

```python
from bsg_api.models.suggestion_link import SuggestionLink

# TODO update the JSON string below
json = "{}"
# create an instance of SuggestionLink from a JSON string
suggestion_link_instance = SuggestionLink.from_json(json)
# print the JSON string representation of the object
print(SuggestionLink.to_json())

# convert the object into a dict
suggestion_link_dict = suggestion_link_instance.to_dict()
# create an instance of SuggestionLink from a dict
suggestion_link_from_dict = SuggestionLink.from_dict(suggestion_link_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

