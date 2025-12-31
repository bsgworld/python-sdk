# BalanceSchema


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **balance** | **float** | Current amount of funds on the account balance | [optional]  |
| **currency** | **str** | The currency code of the account. Specified according to the ISO-4217 standard | [optional]  |
| **credit** | **float** | Available credit limit of the account by the postpay type | [optional]  |

## Example

```python
from bsg_api.models.balance_schema import BalanceSchema

# TODO update the JSON string below
json = "{}"
# create an instance of BalanceSchema from a JSON string
balance_schema_instance = BalanceSchema.from_json(json)
# print the JSON string representation of the object
print(BalanceSchema.to_json())

# convert the object into a dict
balance_schema_dict = balance_schema_instance.to_dict()
# create an instance of BalanceSchema from a dict
balance_schema_from_dict = BalanceSchema.from_dict(balance_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

