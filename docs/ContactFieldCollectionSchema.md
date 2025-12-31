# ContactFieldCollectionSchema

Contact fields list

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ContactFieldSchema]**](ContactFieldSchema.md) | List of contact fields | [optional]  |

## Example

```python
from bsg_api.models.contact_field_collection_schema import ContactFieldCollectionSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldCollectionSchema from a JSON string
contact_field_collection_schema_instance = ContactFieldCollectionSchema.from_json(json)
# print the JSON string representation of the object
print(ContactFieldCollectionSchema.to_json())

# convert the object into a dict
contact_field_collection_schema_dict = contact_field_collection_schema_instance.to_dict()
# create an instance of ContactFieldCollectionSchema from a dict
contact_field_collection_schema_from_dict = ContactFieldCollectionSchema.from_dict(contact_field_collection_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

