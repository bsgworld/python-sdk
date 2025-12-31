# DomainStoreRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | short domain |  |
| **not_found_page** | **str** | Url to redirect if original link return status 404 not found | [optional]  |
| **slug_type** | [**ShortDomainSlugType**](ShortDomainSlugType.md) |  |  |

## Example

```python
from bsg_api.models.domain_store_request import DomainStoreRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DomainStoreRequest from a JSON string
domain_store_request_instance = DomainStoreRequest.from_json(json)
# print the JSON string representation of the object
print(DomainStoreRequest.to_json())

# convert the object into a dict
domain_store_request_dict = domain_store_request_instance.to_dict()
# create an instance of DomainStoreRequest from a dict
domain_store_request_from_dict = DomainStoreRequest.from_dict(domain_store_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

