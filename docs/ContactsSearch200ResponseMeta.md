# ContactsSearch200ResponseMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**ContactsSearch200ResponseMetaPage**](ContactsSearch200ResponseMetaPage.md) |  | [optional]  |
| **search** | [**ContactsSearch200ResponseMetaSearch**](ContactsSearch200ResponseMetaSearch.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contacts_search200_response_meta import ContactsSearch200ResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of ContactsSearch200ResponseMeta from a JSON string
contacts_search200_response_meta_instance = ContactsSearch200ResponseMeta.from_json(json)
# print the JSON string representation of the object
print(ContactsSearch200ResponseMeta.to_json())

# convert the object into a dict
contacts_search200_response_meta_dict = contacts_search200_response_meta_instance.to_dict()
# create an instance of ContactsSearch200ResponseMeta from a dict
contacts_search200_response_meta_from_dict = ContactsSearch200ResponseMeta.from_dict(contacts_search200_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

