# ContactCreate201Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**ContactSchema**](ContactSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contact_create201_response import ContactCreate201Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactCreate201Response from a JSON string
contact_create201_response_instance = ContactCreate201Response.from_json(json)
# print the JSON string representation of the object
print(ContactCreate201Response.to_json())

# convert the object into a dict
contact_create201_response_dict = contact_create201_response_instance.to_dict()
# create an instance of ContactCreate201Response from a dict
contact_create201_response_from_dict = ContactCreate201Response.from_dict(contact_create201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

