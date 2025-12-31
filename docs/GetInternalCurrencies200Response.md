# GetInternalCurrencies200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[GetInternalCurrencies200ResponseDataItem]**](GetInternalCurrencies200ResponseDataItem.md) |  |  |

## Example

```python
from bsg_api.models.get_internal_currencies200_response import GetInternalCurrencies200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetInternalCurrencies200Response from a JSON string
get_internal_currencies200_response_instance = GetInternalCurrencies200Response.from_json(json)
# print the JSON string representation of the object
print(GetInternalCurrencies200Response.to_json())

# convert the object into a dict
get_internal_currencies200_response_dict = get_internal_currencies200_response_instance.to_dict()
# create an instance of GetInternalCurrencies200Response from a dict
get_internal_currencies200_response_from_dict = GetInternalCurrencies200Response.from_dict(get_internal_currencies200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

