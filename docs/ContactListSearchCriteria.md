# ContactListSearchCriteria

Search criteria

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **var_field** | [**ContactGroupSearchField**](ContactGroupSearchField.md) |  | [optional]  |
| **operator** | [**SearchOperator**](SearchOperator.md) |  | [optional]  |
| **value** | **str** | Value to to find using search[field] and search[operator] | [optional]  |

## Example

```python
from bsg_api.models.contact_list_search_criteria import ContactListSearchCriteria

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListSearchCriteria from a JSON string
contact_list_search_criteria_instance = ContactListSearchCriteria.from_json(json)
# print the JSON string representation of the object
print(ContactListSearchCriteria.to_json())

# convert the object into a dict
contact_list_search_criteria_dict = contact_list_search_criteria_instance.to_dict()
# create an instance of ContactListSearchCriteria from a dict
contact_list_search_criteria_from_dict = ContactListSearchCriteria.from_dict(contact_list_search_criteria_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

