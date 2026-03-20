# Recipients


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phones** | [**List[Phone]**](Phone.md) | The list of objects containing information about the mobile phone number (number) and (reference_id) to send a message to | [optional]  |
| **groups** | **List[int]** | An array of lists (list id) with contacts from the address book to which RCS campaigns are to be sent. id of the lists can be obtained: using the Get [lists API](#tag/Contact-List) in your account [Contact Book → Lists](https://app.bsg.world/addressbook/lists) | [optional]  |

## Example

```python
from bsg_api.models.recipients import Recipients

# TODO update the JSON string below
json = "{}"
# create an instance of Recipients from a JSON string
recipients_instance = Recipients.from_json(json)
# print the JSON string representation of the object
print(Recipients.to_json())

# convert the object into a dict
recipients_dict = recipients_instance.to_dict()
# create an instance of Recipients from a dict
recipients_from_dict = Recipients.from_dict(recipients_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

