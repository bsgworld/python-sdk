# ContactsSearch200ResponseMetaSearch

Search criteria

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_field** | **str** | Field for search. Possible values: id, phone, group_id, date, {field_id}  {field_id} – custom field ID; can be got from [GET /api/contacts/fields](#operation/contact_fields) | [optional]  |
| **operator** | [**SearchOperator**](SearchOperator.md) |  | [optional]  |
| **value** | **str** | Value to to find using search[field] and search[operator] | [optional]  |

## Example

```python
from bsg_api.models.contacts_search200_response_meta_search import ContactsSearch200ResponseMetaSearch

# TODO update the JSON string below
json = "{}"
# create an instance of ContactsSearch200ResponseMetaSearch from a JSON string
contacts_search200_response_meta_search_instance = ContactsSearch200ResponseMetaSearch.from_json(json)
# print the JSON string representation of the object
print(ContactsSearch200ResponseMetaSearch.to_json())

# convert the object into a dict
contacts_search200_response_meta_search_dict = contacts_search200_response_meta_search_instance.to_dict()
# create an instance of ContactsSearch200ResponseMetaSearch from a dict
contacts_search200_response_meta_search_from_dict = ContactsSearch200ResponseMetaSearch.from_dict(contacts_search200_response_meta_search_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

