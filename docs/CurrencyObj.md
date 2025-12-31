# CurrencyObj


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **fallback_value** | **str** | Default text if localization fails. |  |
| **code** | **str** | Currency code as defined in ISO 4217. |  |
| **amount_1000** | **float** | Amount multiplied by 1000. |  |

## Example

```python
from bsg_api.models.currency_obj import CurrencyObj

# TODO update the JSON string below
json = "{}"
# create an instance of CurrencyObj from a JSON string
currency_obj_instance = CurrencyObj.from_json(json)
# print the JSON string representation of the object
print(CurrencyObj.to_json())

# convert the object into a dict
currency_obj_dict = currency_obj_instance.to_dict()
# create an instance of CurrencyObj from a dict
currency_obj_from_dict = CurrencyObj.from_dict(currency_obj_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

