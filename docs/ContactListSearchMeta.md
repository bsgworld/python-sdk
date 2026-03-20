# ContactListSearchMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**MetaPage**](MetaPage.md) |  | [optional]  |
| **search** | [**ContactListSearchCriteria**](ContactListSearchCriteria.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contact_list_search_meta import ContactListSearchMeta

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListSearchMeta from a JSON string
contact_list_search_meta_instance = ContactListSearchMeta.from_json(json)
# print the JSON string representation of the object
print(ContactListSearchMeta.to_json())

# convert the object into a dict
contact_list_search_meta_dict = contact_list_search_meta_instance.to_dict()
# create an instance of ContactListSearchMeta from a dict
contact_list_search_meta_from_dict = ContactListSearchMeta.from_dict(contact_list_search_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

