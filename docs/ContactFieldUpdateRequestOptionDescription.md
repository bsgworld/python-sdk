# ContactFieldUpdateRequestOptionDescription


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **str** | Description of the custom contact field | [optional]  |

## Example

```python
from bsg_api.models.contact_field_update_request_option_description import ContactFieldUpdateRequestOptionDescription

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldUpdateRequestOptionDescription from a JSON string
contact_field_update_request_option_description_instance = ContactFieldUpdateRequestOptionDescription.from_json(json)
# print the JSON string representation of the object
print(ContactFieldUpdateRequestOptionDescription.to_json())

# convert the object into a dict
contact_field_update_request_option_description_dict = contact_field_update_request_option_description_instance.to_dict()
# create an instance of ContactFieldUpdateRequestOptionDescription from a dict
contact_field_update_request_option_description_from_dict = ContactFieldUpdateRequestOptionDescription.from_dict(contact_field_update_request_option_description_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

