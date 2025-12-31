# AccountBalance200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**BalanceSchema**](BalanceSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.account_balance200_response import AccountBalance200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AccountBalance200Response from a JSON string
account_balance200_response_instance = AccountBalance200Response.from_json(json)
# print the JSON string representation of the object
print(AccountBalance200Response.to_json())

# convert the object into a dict
account_balance200_response_dict = account_balance200_response_instance.to_dict()
# create an instance of AccountBalance200Response from a dict
account_balance200_response_from_dict = AccountBalance200Response.from_dict(account_balance200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

