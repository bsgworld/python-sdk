# LinkUpdateRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **str** | Name of short link. like a comment | [optional]  |
| **slug** | **str** | part of short link after domain | [optional]  |
| **original_link** | **str** | Original link where to short link will redirect | [optional]  |

## Example

```python
from bsg_api.models.link_update_request import LinkUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of LinkUpdateRequest from a JSON string
link_update_request_instance = LinkUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(LinkUpdateRequest.to_json())

# convert the object into a dict
link_update_request_dict = link_update_request_instance.to_dict()
# create an instance of LinkUpdateRequest from a dict
link_update_request_from_dict = LinkUpdateRequest.from_dict(link_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

