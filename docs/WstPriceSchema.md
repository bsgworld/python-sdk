# WstPriceSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **str** |  | [optional]  |
| **price** | **float** |  | [optional]  |
| **currency** | **str** |  | [optional]  |

## Example

```python
from bsg_api.models.wst_price_schema import WstPriceSchema

# TODO update the JSON string below
json = "{}"
# create an instance of WstPriceSchema from a JSON string
wst_price_schema_instance = WstPriceSchema.from_json(json)
# print the JSON string representation of the object
print(WstPriceSchema.to_json())

# convert the object into a dict
wst_price_schema_dict = wst_price_schema_instance.to_dict()
# create an instance of WstPriceSchema from a dict
wst_price_schema_from_dict = WstPriceSchema.from_dict(wst_price_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

