# ContactsSearch200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ContactSchema]**](ContactSchema.md) | List of searched contacts | [optional]  |
| **meta** | [**ContactsSearch200ResponseMeta**](ContactsSearch200ResponseMeta.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contacts_search200_response import ContactsSearch200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactsSearch200Response from a JSON string
contacts_search200_response_instance = ContactsSearch200Response.from_json(json)
# print the JSON string representation of the object
print(ContactsSearch200Response.to_json())

# convert the object into a dict
contacts_search200_response_dict = contacts_search200_response_instance.to_dict()
# create an instance of ContactsSearch200Response from a dict
contacts_search200_response_from_dict = ContactsSearch200Response.from_dict(contacts_search200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

