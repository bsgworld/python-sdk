# ContactFieldSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Custom field ID | [optional]  |
| **name** | **str** | The name of the custom field for the contacts | [optional]  |
| **type** | [**ContactFieldType**](ContactFieldType.md) |  | [optional]  |
| **description** | **str** | Description of the custom contact field | [optional]  |
| **is_visible** | **bool** | Whether the field is displayed: true or false value | [optional] [default to True] |

## Example

```python
from bsg_api.models.contact_field_schema import ContactFieldSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldSchema from a JSON string
contact_field_schema_instance = ContactFieldSchema.from_json(json)
# print the JSON string representation of the object
print(ContactFieldSchema.to_json())

# convert the object into a dict
contact_field_schema_dict = contact_field_schema_instance.to_dict()
# create an instance of ContactFieldSchema from a dict
contact_field_schema_from_dict = ContactFieldSchema.from_dict(contact_field_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

