# ContactUpdate200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**ContactSchema**](ContactSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contact_update200_response import ContactUpdate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ContactUpdate200Response from a JSON string
contact_update200_response_instance = ContactUpdate200Response.from_json(json)
# print the JSON string representation of the object
print(ContactUpdate200Response.to_json())

# convert the object into a dict
contact_update200_response_dict = contact_update200_response_instance.to_dict()
# create an instance of ContactUpdate200Response from a dict
contact_update200_response_from_dict = ContactUpdate200Response.from_dict(contact_update200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

