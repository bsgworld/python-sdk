# ContactListSearch200ResponseMeta

Information about search criteria and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**ContactListSearch200ResponseMetaPage**](ContactListSearch200ResponseMetaPage.md) |  | [optional]  |
| **search** | [**ContactListSearch200ResponseMetaSearch**](ContactListSearch200ResponseMetaSearch.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contact_list_search200_response_meta import ContactListSearch200ResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListSearch200ResponseMeta from a JSON string
contact_list_search200_response_meta_instance = ContactListSearch200ResponseMeta.from_json(json)
# print the JSON string representation of the object
print(ContactListSearch200ResponseMeta.to_json())

# convert the object into a dict
contact_list_search200_response_meta_dict = contact_list_search200_response_meta_instance.to_dict()
# create an instance of ContactListSearch200ResponseMeta from a dict
contact_list_search200_response_meta_from_dict = ContactListSearch200ResponseMeta.from_dict(contact_list_search200_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

