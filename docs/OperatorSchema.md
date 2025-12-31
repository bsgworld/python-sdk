# OperatorSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** |  | [optional]  |
| **mcc** | **int** |  | [optional]  |
| **mnc** | **int** |  | [optional]  |
| **brand** | **str** |  | [optional]  |
| **name** | **str** |  | [optional]  |
| **price** | **float** |  | [optional]  |
| **currency** | **str** |  | [optional]  |
| **price_type** | **str** |  | [optional]  |
| **sender_registration** | **bool** |  | [optional]  |

## Example

```python
from bsg_api.models.operator_schema import OperatorSchema

# TODO update the JSON string below
json = "{}"
# create an instance of OperatorSchema from a JSON string
operator_schema_instance = OperatorSchema.from_json(json)
# print the JSON string representation of the object
print(OperatorSchema.to_json())

# convert the object into a dict
operator_schema_dict = operator_schema_instance.to_dict()
# create an instance of OperatorSchema from a dict
operator_schema_from_dict = OperatorSchema.from_dict(operator_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

