# ContactListUpdateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | Name of the contact list |  |
| **description** | **str** | Description of the contact list | [optional]  |
| **default** | **bool** | Specifies whether the contact list is a default one | [optional] [default to False] |

## Example

```python
from bsg_api.models.contact_list_update_request import ContactListUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListUpdateRequest from a JSON string
contact_list_update_request_instance = ContactListUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(ContactListUpdateRequest.to_json())

# convert the object into a dict
contact_list_update_request_dict = contact_list_update_request_instance.to_dict()
# create an instance of ContactListUpdateRequest from a dict
contact_list_update_request_from_dict = ContactListUpdateRequest.from_dict(contact_list_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

