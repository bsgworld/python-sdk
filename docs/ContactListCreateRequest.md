# ContactListCreateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | Name of the contact list |  |
| **description** | **str** | Description of the contact list | [optional]  |
| **default** | **bool** | Specifies whether the contact list is a default one | [optional] [default to False] |

## Example

```python
from bsg_api.models.contact_list_create_request import ContactListCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListCreateRequest from a JSON string
contact_list_create_request_instance = ContactListCreateRequest.from_json(json)
# print the JSON string representation of the object
print(ContactListCreateRequest.to_json())

# convert the object into a dict
contact_list_create_request_dict = contact_list_create_request_instance.to_dict()
# create an instance of ContactListCreateRequest from a dict
contact_list_create_request_from_dict = ContactListCreateRequest.from_dict(contact_list_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

