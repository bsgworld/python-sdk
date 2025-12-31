# TokenSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bearer** | **str** | Token for authorization of API queries. | [optional]  |

## Example

```python
from bsg_api.models.token_schema import TokenSchema

# TODO update the JSON string below
json = "{}"
# create an instance of TokenSchema from a JSON string
token_schema_instance = TokenSchema.from_json(json)
# print the JSON string representation of the object
print(TokenSchema.to_json())

# convert the object into a dict
token_schema_dict = token_schema_instance.to_dict()
# create an instance of TokenSchema from a dict
token_schema_from_dict = TokenSchema.from_dict(token_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

