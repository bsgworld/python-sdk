# ContactListSearch200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ContactGroupSearchSchema]**](ContactGroupSearchSchema.md) |  | [optional]  |
| **meta** | [**ContactListSearch200ResponseMeta**](ContactListSearch200ResponseMeta.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contact_list_search200_response import ContactListSearch200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactListSearch200Response from a JSON string
contact_list_search200_response_instance = ContactListSearch200Response.from_json(json)
# print the JSON string representation of the object
print(ContactListSearch200Response.to_json())

# convert the object into a dict
contact_list_search200_response_dict = contact_list_search200_response_instance.to_dict()
# create an instance of ContactListSearch200Response from a dict
contact_list_search200_response_from_dict = ContactListSearch200Response.from_dict(contact_list_search200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

