# AccountTariffs200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[TariffSchema]**](TariffSchema.md) |  | [optional]  |
| **total** | **int** | Total items count at all of the pages | [optional]  |

## Example

```python
from bsg_api.models.account_tariffs200_response import AccountTariffs200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AccountTariffs200Response from a JSON string
account_tariffs200_response_instance = AccountTariffs200Response.from_json(json)
# print the JSON string representation of the object
print(AccountTariffs200Response.to_json())

# convert the object into a dict
account_tariffs200_response_dict = account_tariffs200_response_instance.to_dict()
# create an instance of AccountTariffs200Response from a dict
account_tariffs200_response_from_dict = AccountTariffs200Response.from_dict(account_tariffs200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

