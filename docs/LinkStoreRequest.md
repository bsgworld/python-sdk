# LinkStoreRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **domain_id** | **str** | Domain ID from connected short domains from [account](https://app.bsg.world/url-shortener/domains)  **Please note:** *only domains in **active** status accepted* |  |
| **link** | **str** | Original link where to short link will redirect |  |

## Example

```python
from bsg_api.models.link_store_request import LinkStoreRequest

# TODO update the JSON string below
json = "{}"
# create an instance of LinkStoreRequest from a JSON string
link_store_request_instance = LinkStoreRequest.from_json(json)
# print the JSON string representation of the object
print(LinkStoreRequest.to_json())

# convert the object into a dict
link_store_request_dict = link_store_request_instance.to_dict()
# create an instance of LinkStoreRequest from a dict
link_store_request_from_dict = LinkStoreRequest.from_dict(link_store_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

