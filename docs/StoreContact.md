# StoreContact

Contact data

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | **int** | Contact’s phone number |  |
| **groups** | [**List[ContactGroupSchema]**](ContactGroupSchema.md) | contains embedded data of the list where the contact is added | [optional]  |
| **fields** | [**List[ContactFieldValuePair]**](ContactFieldValuePair.md) | Array of custom fields values | [optional]  |

## Example

```python
from bsg_api.models.store_contact import StoreContact

# TODO update the JSON string below
json = "{}"
# create an instance of StoreContact from a JSON string
store_contact_instance = StoreContact.from_json(json)
# print the JSON string representation of the object
print(StoreContact.to_json())

# convert the object into a dict
store_contact_dict = store_contact_instance.to_dict()
# create an instance of StoreContact from a dict
store_contact_from_dict = StoreContact.from_dict(store_contact_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

