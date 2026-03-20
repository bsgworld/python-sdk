# CurrencyItem


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** |  | [optional]  |
| **ratio** | **float** | EUR exchange rate | [optional]  |
| **nominal** | **int** |  | [optional]  |
| **var_date** | **object** |  | [optional]  |

## Example

```python
from bsg_api.models.currency_item import CurrencyItem

# TODO update the JSON string below
json = "{}"
# create an instance of CurrencyItem from a JSON string
currency_item_instance = CurrencyItem.from_json(json)
# print the JSON string representation of the object
print(CurrencyItem.to_json())

# convert the object into a dict
currency_item_dict = currency_item_instance.to_dict()
# create an instance of CurrencyItem from a dict
currency_item_from_dict = CurrencyItem.from_dict(currency_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

