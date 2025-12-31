# ContactsSearch200ResponseMetaPage

Pagination parameters and total results count

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **int** | Total items count at all of the pages | [optional]  |
| **limit** | **int** | Limit items at one page | [optional]  |
| **offset** | **int** | Get items starting at offset | [optional] [default to 0] |

## Example

```python
from bsg_api.models.contacts_search200_response_meta_page import ContactsSearch200ResponseMetaPage

# TODO update the JSON string below
json = "{}"
# create an instance of ContactsSearch200ResponseMetaPage from a JSON string
contacts_search200_response_meta_page_instance = ContactsSearch200ResponseMetaPage.from_json(json)
# print the JSON string representation of the object
print(ContactsSearch200ResponseMetaPage.to_json())

# convert the object into a dict
contacts_search200_response_meta_page_dict = contacts_search200_response_meta_page_instance.to_dict()
# create an instance of ContactsSearch200ResponseMetaPage from a dict
contacts_search200_response_meta_page_from_dict = ContactsSearch200ResponseMetaPage.from_dict(contacts_search200_response_meta_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

