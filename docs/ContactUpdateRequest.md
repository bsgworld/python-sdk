# ContactUpdateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | **int** | Contact’s phone number |  |
| **groups** | [**List[ContactGroupSchema]**](ContactGroupSchema.md) | contains embedded data of the list where the contact is added | [optional]  |
| **fields** | [**List[ContactFieldValuePair]**](ContactFieldValuePair.md) | Array of custom fields values | [optional]  |

## Example

```python
from bsg_api.models.contact_update_request import ContactUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ContactUpdateRequest from a JSON string
contact_update_request_instance = ContactUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(ContactUpdateRequest.to_json())

# convert the object into a dict
contact_update_request_dict = contact_update_request_instance.to_dict()
# create an instance of ContactUpdateRequest from a dict
contact_update_request_from_dict = ContactUpdateRequest.from_dict(contact_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

