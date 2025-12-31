# Contact200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**ContactSchema**](ContactSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.contact200_response import Contact200Response

# TODO update the JSON string below
json = "{}"
# create an instance of Contact200Response from a JSON string
contact200_response_instance = Contact200Response.from_json(json)
# print the JSON string representation of the object
print(Contact200Response.to_json())

# convert the object into a dict
contact200_response_dict = contact200_response_instance.to_dict()
# create an instance of Contact200Response from a dict
contact200_response_from_dict = Contact200Response.from_dict(contact200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

