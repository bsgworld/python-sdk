# TariffSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **float** | Tariff id | [optional]  |
| **name** | **str** | Tariff name | [optional]  |
| **code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **is_active** | **bool** | Indicates whether the tariff is active | [optional]  |
| **is_default** | **bool** | Indicates whether the rate is the default | [optional]  |

## Example

```python
from bsg_api.models.tariff_schema import TariffSchema

# TODO update the JSON string below
json = "{}"
# create an instance of TariffSchema from a JSON string
tariff_schema_instance = TariffSchema.from_json(json)
# print the JSON string representation of the object
print(TariffSchema.to_json())

# convert the object into a dict
tariff_schema_dict = tariff_schema_instance.to_dict()
# create an instance of TariffSchema from a dict
tariff_schema_from_dict = TariffSchema.from_dict(tariff_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

