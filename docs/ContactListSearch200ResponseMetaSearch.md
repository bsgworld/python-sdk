# ContactListSearch200ResponseMetaSearch

Search criteria

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_field** | [**ContactGroupSearchField**](ContactGroupSearchField.md) |  | [optional]  |
| **operator** | [**SearchOperator**](SearchOperator.md) |  | [optional]  |
| **value** | **str** | Value to to find using search[field] and search[operator] | [optional]  |

## Example

```python
from bsg_api.models.contact_list_search200_response_meta_search import ContactListSearch200ResponseMetaSearch

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListSearch200ResponseMetaSearch from a JSON string
contact_list_search200_response_meta_search_instance = ContactListSearch200ResponseMetaSearch.from_json(json)
# print the JSON string representation of the object
print(ContactListSearch200ResponseMetaSearch.to_json())

# convert the object into a dict
contact_list_search200_response_meta_search_dict = contact_list_search200_response_meta_search_instance.to_dict()
# create an instance of ContactListSearch200ResponseMetaSearch from a dict
contact_list_search200_response_meta_search_from_dict = ContactListSearch200ResponseMetaSearch.from_dict(contact_list_search200_response_meta_search_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

