# RcsSingle200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**MessageInfo**](MessageInfo.md) |  | [optional]  |

## Example

```python
from bsg_api.models.rcs_single200_response import RcsSingle200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RcsSingle200Response from a JSON string
rcs_single200_response_instance = RcsSingle200Response.from_json(json)
# print the JSON string representation of the object
print(RcsSingle200Response.to_json())

# convert the object into a dict
rcs_single200_response_dict = rcs_single200_response_instance.to_dict()
# create an instance of RcsSingle200Response from a dict
rcs_single200_response_from_dict = RcsSingle200Response.from_dict(rcs_single200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

