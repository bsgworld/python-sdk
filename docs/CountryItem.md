# CountryItem


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **object** |  | [optional]  |

## Example

```python
from bsg_api.models.country_item import CountryItem

# TODO update the JSON string below
json = "{}"
# create an instance of CountryItem from a JSON string
country_item_instance = CountryItem.from_json(json)
# print the JSON string representation of the object
print(CountryItem.to_json())

# convert the object into a dict
country_item_dict = country_item_instance.to_dict()
# create an instance of CountryItem from a dict
country_item_from_dict = CountryItem.from_dict(country_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

