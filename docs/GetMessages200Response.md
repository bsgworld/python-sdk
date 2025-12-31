# GetMessages200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[MessageApiSchema]**](MessageApiSchema.md) |  | [optional]  |
| **meta** | [**GetMessages200ResponseMeta**](GetMessages200ResponseMeta.md) |  | [optional]  |

## Example

```python
from bsg_api.models.get_messages200_response import GetMessages200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetMessages200Response from a JSON string
get_messages200_response_instance = GetMessages200Response.from_json(json)
# print the JSON string representation of the object
print(GetMessages200Response.to_json())

# convert the object into a dict
get_messages200_response_dict = get_messages200_response_instance.to_dict()
# create an instance of GetMessages200Response from a dict
get_messages200_response_from_dict = GetMessages200Response.from_dict(get_messages200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

