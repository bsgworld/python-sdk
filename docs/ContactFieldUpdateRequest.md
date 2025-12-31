# ContactFieldUpdateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | The name of the custom field for the contacts | [optional]  |
| **description** | **str** | Description of the custom contact field | [optional]  |
| **is_visible** | **bool** | Whether the field is displayed: true or false value | [optional] [default to True] |

## Example

```python
from bsg_api.models.contact_field_update_request import ContactFieldUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldUpdateRequest from a JSON string
contact_field_update_request_instance = ContactFieldUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(ContactFieldUpdateRequest.to_json())

# convert the object into a dict
contact_field_update_request_dict = contact_field_update_request_instance.to_dict()
# create an instance of ContactFieldUpdateRequest from a dict
contact_field_update_request_from_dict = ContactFieldUpdateRequest.from_dict(contact_field_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

