# ContactFieldValuePair

contains embedded custom fields data

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | Custom field ID | [optional]  |
| **value** | **str** | Custom field data | [optional]  |

## Example

```python
from bsg_api.models.contact_field_value_pair import ContactFieldValuePair

# TODO update the JSON string below
json = "{}"
# create an instance of ContactFieldValuePair from a JSON string
contact_field_value_pair_instance = ContactFieldValuePair.from_json(json)
# print the JSON string representation of the object
print(ContactFieldValuePair.to_json())

# convert the object into a dict
contact_field_value_pair_dict = contact_field_value_pair_instance.to_dict()
# create an instance of ContactFieldValuePair from a dict
contact_field_value_pair_from_dict = ContactFieldValuePair.from_dict(contact_field_value_pair_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

