# DomainUpdateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **not_found_page** | **str** | Url to redirect if original link return status 404 not found | [optional]  |
| **slug_type** | [**ShortDomainSlugType**](ShortDomainSlugType.md) |  | [optional]  |
| **is_default** | **bool** | This domain is default for generating short links | [optional] [default to True] |

## Example

```python
from bsg_api.models.domain_update_request import DomainUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DomainUpdateRequest from a JSON string
domain_update_request_instance = DomainUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(DomainUpdateRequest.to_json())

# convert the object into a dict
domain_update_request_dict = domain_update_request_instance.to_dict()
# create an instance of DomainUpdateRequest from a dict
domain_update_request_from_dict = DomainUpdateRequest.from_dict(domain_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

