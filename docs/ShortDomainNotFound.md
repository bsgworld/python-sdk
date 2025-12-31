# ShortDomainNotFound


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | Domain not found | [optional]  |

## Example

```python
from bsg_api.models.short_domain_not_found import ShortDomainNotFound

# TODO update the JSON string below
json = "{}"
# create an instance of ShortDomainNotFound from a JSON string
short_domain_not_found_instance = ShortDomainNotFound.from_json(json)
# print the JSON string representation of the object
print(ShortDomainNotFound.to_json())

# convert the object into a dict
short_domain_not_found_dict = short_domain_not_found_instance.to_dict()
# create an instance of ShortDomainNotFound from a dict
short_domain_not_found_from_dict = ShortDomainNotFound.from_dict(short_domain_not_found_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

