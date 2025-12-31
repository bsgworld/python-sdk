# MessagePriceObject

Message price value and currency

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **value** | **float** | Message price | [optional]  |
| **currency** | **str** | The currency code of the account. Specified according to the ISO-4217 standard | [optional]  |

## Example

```python
from bsg_api.models.message_price_object import MessagePriceObject

# TODO update the JSON string below
json = "{}"
# create an instance of MessagePriceObject from a JSON string
message_price_object_instance = MessagePriceObject.from_json(json)
# print the JSON string representation of the object
print(MessagePriceObject.to_json())

# convert the object into a dict
message_price_object_dict = message_price_object_instance.to_dict()
# create an instance of MessagePriceObject from a dict
message_price_object_from_dict = MessagePriceObject.from_dict(message_price_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

