# ContactLists200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ContactGroupSchema]**](ContactGroupSchema.md) |  | [optional]  |
| **total** | **int** | Total items count at all of the pages | [optional]  |

## Example

```python
from bsg_api.models.contact_lists200_response import ContactLists200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactLists200Response from a JSON string
contact_lists200_response_instance = ContactLists200Response.from_json(json)
# print the JSON string representation of the object
print(ContactLists200Response.to_json())

# convert the object into a dict
contact_lists200_response_dict = contact_lists200_response_instance.to_dict()
# create an instance of ContactLists200Response from a dict
contact_lists200_response_from_dict = ContactLists200Response.from_dict(contact_lists200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

