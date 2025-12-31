# ContactSchema

Contact data

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Contact ID in the platform personal account, which is generated automatically when a contact is added to the Contact Book | [optional]  |
| **phone** | **int** | Contact’s phone number | [optional]  |
| **fields** | **List[Dict[str, str]]** | List of contact custom field values | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **groups** | [**List[ContactGroupSchema]**](ContactGroupSchema.md) | contains embedded data of the list where the contact is added | [optional]  |
| **hlr_status** | **str** | Last hlr check status of contact phone number | [optional]  |
| **hlr_last_check** | **datetime** | Last hlr check time of contact phone number | [optional]  |

## Example

```python
from bsg_api.models.contact_schema import ContactSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ContactSchema from a JSON string
contact_schema_instance = ContactSchema.from_json(json)
# print the JSON string representation of the object
print(ContactSchema.to_json())

# convert the object into a dict
contact_schema_dict = contact_schema_instance.to_dict()
# create an instance of ContactSchema from a dict
contact_schema_from_dict = ContactSchema.from_dict(contact_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

