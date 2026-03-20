# ContactFieldUpdateRequestOptionName


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | The name of the custom field for the contacts | [optional]  |

## Example

```python
from bsg_api.models.contact_field_update_request_option_name import ContactFieldUpdateRequestOptionName

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldUpdateRequestOptionName from a JSON string
contact_field_update_request_option_name_instance = ContactFieldUpdateRequestOptionName.from_json(json)
# print the JSON string representation of the object
print(ContactFieldUpdateRequestOptionName.to_json())

# convert the object into a dict
contact_field_update_request_option_name_dict = contact_field_update_request_option_name_instance.to_dict()
# create an instance of ContactFieldUpdateRequestOptionName from a dict
contact_field_update_request_option_name_from_dict = ContactFieldUpdateRequestOptionName.from_dict(contact_field_update_request_option_name_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

