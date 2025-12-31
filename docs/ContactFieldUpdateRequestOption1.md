# ContactFieldUpdateRequestOption1


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | The name of the custom field for the contacts | [optional]  |

## Example

```python
from bsg_api.models.contact_field_update_request_option1 import ContactFieldUpdateRequestOption1

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldUpdateRequestOption1 from a JSON string
contact_field_update_request_option1_instance = ContactFieldUpdateRequestOption1.from_json(json)
# print the JSON string representation of the object
print(ContactFieldUpdateRequestOption1.to_json())

# convert the object into a dict
contact_field_update_request_option1_dict = contact_field_update_request_option1_instance.to_dict()
# create an instance of ContactFieldUpdateRequestOption1 from a dict
contact_field_update_request_option1_from_dict = ContactFieldUpdateRequestOption1.from_dict(contact_field_update_request_option1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

