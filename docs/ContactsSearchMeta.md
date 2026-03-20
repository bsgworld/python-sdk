# ContactsSearchMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**MetaPage**](MetaPage.md) |  | [optional]  |
| **search** | [**ContactsSearchCriteria**](ContactsSearchCriteria.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contacts_search_meta import ContactsSearchMeta

# TODO update the JSON string below
json = "{}"
# create an instance of ContactsSearchMeta from a JSON string
contacts_search_meta_instance = ContactsSearchMeta.from_json(json)
# print the JSON string representation of the object
print(ContactsSearchMeta.to_json())

# convert the object into a dict
contacts_search_meta_dict = contacts_search_meta_instance.to_dict()
# create an instance of ContactsSearchMeta from a dict
contacts_search_meta_from_dict = ContactsSearchMeta.from_dict(contacts_search_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

