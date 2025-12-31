# Contacts200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[ContactSchema]**](ContactSchema.md) | list of contacts | [optional]  |
| **total** | **int** | Total items count at all of the pages | [optional]  |

## Example

```python
from bsg_api.models.contacts200_response import Contacts200Response

# TODO update the JSON string below
json = "{}"
# create an instance of Contacts200Response from a JSON string
contacts200_response_instance = Contacts200Response.from_json(json)
# print the JSON string representation of the object
print(Contacts200Response.to_json())

# convert the object into a dict
contacts200_response_dict = contacts200_response_instance.to_dict()
# create an instance of Contacts200Response from a dict
contacts200_response_from_dict = Contacts200Response.from_dict(contacts200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

