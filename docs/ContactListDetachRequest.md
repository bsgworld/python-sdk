# ContactListDetachRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contacts** | **List[int]** | contacts Id |  |
| **groups** | **List[int]** | Contact lists IDs |  |

## Example

```python
from bsg_api.models.contact_list_detach_request import ContactListDetachRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListDetachRequest from a JSON string
contact_list_detach_request_instance = ContactListDetachRequest.from_json(json)
# print the JSON string representation of the object
print(ContactListDetachRequest.to_json())

# convert the object into a dict
contact_list_detach_request_dict = contact_list_detach_request_instance.to_dict()
# create an instance of ContactListDetachRequest from a dict
contact_list_detach_request_from_dict = ContactListDetachRequest.from_dict(contact_list_detach_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

