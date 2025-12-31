# ContactGroupSearchSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | ID of the contact list. generated automatically when creating a [contact list](#operation/contact_list_create) | [optional]  |
| **name** | **str** | Name of the contact list | [optional]  |
| **description** | **str** | Description of the contact list | [optional]  |
| **is_default** | **bool** | Specifies whether the contact list is a default one | [optional] [default to False] |
| **items** | **int** | Total number of contacts in this list | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |

## Example

```python
from bsg_api.models.contact_group_search_schema import ContactGroupSearchSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ContactGroupSearchSchema from a JSON string
contact_group_search_schema_instance = ContactGroupSearchSchema.from_json(json)
# print the JSON string representation of the object
print(ContactGroupSearchSchema.to_json())

# convert the object into a dict
contact_group_search_schema_dict = contact_group_search_schema_instance.to_dict()
# create an instance of ContactGroupSearchSchema from a dict
contact_group_search_schema_from_dict = ContactGroupSearchSchema.from_dict(contact_group_search_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

