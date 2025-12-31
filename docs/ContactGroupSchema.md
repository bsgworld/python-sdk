# ContactGroupSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | ID of the contact list. generated automatically when creating a [contact list](#operation/contact_list_create) | [optional]  |
| **name** | **str** | Name of the contact list | [optional]  |
| **description** | **str** | Description of the contact list | [optional]  |
| **default** | **bool** | Specifies whether the contact list is a default one | [optional] [default to False] |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **items** | **int** | Total number of contacts in this list | [optional]  |
| **stop_list_count** | **int** | The number of contacts from the list that are in the stop list of SMS and Viber | [optional]  |

## Example

```python
from bsg_api.models.contact_group_schema import ContactGroupSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ContactGroupSchema from a JSON string
contact_group_schema_instance = ContactGroupSchema.from_json(json)
# print the JSON string representation of the object
print(ContactGroupSchema.to_json())

# convert the object into a dict
contact_group_schema_dict = contact_group_schema_instance.to_dict()
# create an instance of ContactGroupSchema from a dict
contact_group_schema_from_dict = ContactGroupSchema.from_dict(contact_group_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

