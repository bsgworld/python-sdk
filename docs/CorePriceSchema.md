# CorePriceSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tariff** | **int** |  | [optional]  |
| **limitation_info** | **str** |  | [optional]  |
| **country_id** | **str** |  | [optional]  |
| **operators** | [**List[OperatorSchema]**](OperatorSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.core_price_schema import CorePriceSchema

# TODO update the JSON string below
json = "{}"
# create an instance of CorePriceSchema from a JSON string
core_price_schema_instance = CorePriceSchema.from_json(json)
# print the JSON string representation of the object
print(CorePriceSchema.to_json())

# convert the object into a dict
core_price_schema_dict = core_price_schema_instance.to_dict()
# create an instance of CorePriceSchema from a dict
core_price_schema_from_dict = CorePriceSchema.from_dict(core_price_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

