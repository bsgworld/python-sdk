# GetInternalCurrencies200ResponseDataItem


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** |  | [optional]  |
| **ratio** | **float** | EUR exchange rate | [optional]  |
| **nominal** | **int** |  | [optional]  |
| **var_date** | **object** |  | [optional]  |

## Example

```python
from bsg_api.models.get_internal_currencies200_response_data_item import GetInternalCurrencies200ResponseDataItem

# TODO update the JSON string below
json = "{}"
# create an instance of GetInternalCurrencies200ResponseDataItem from a JSON string
get_internal_currencies200_response_data_item_instance = GetInternalCurrencies200ResponseDataItem.from_json(json)
# print the JSON string representation of the object
print(GetInternalCurrencies200ResponseDataItem.to_json())

# convert the object into a dict
get_internal_currencies200_response_data_item_dict = get_internal_currencies200_response_data_item_instance.to_dict()
# create an instance of GetInternalCurrencies200ResponseDataItem from a dict
get_internal_currencies200_response_data_item_from_dict = GetInternalCurrencies200ResponseDataItem.from_dict(get_internal_currencies200_response_data_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

