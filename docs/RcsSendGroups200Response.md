# RcsSendGroups200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**CampaignSchema**](CampaignSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.rcs_send_groups200_response import RcsSendGroups200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RcsSendGroups200Response from a JSON string
rcs_send_groups200_response_instance = RcsSendGroups200Response.from_json(json)
# print the JSON string representation of the object
print(RcsSendGroups200Response.to_json())

# convert the object into a dict
rcs_send_groups200_response_dict = rcs_send_groups200_response_instance.to_dict()
# create an instance of RcsSendGroups200Response from a dict
rcs_send_groups200_response_from_dict = RcsSendGroups200Response.from_dict(rcs_send_groups200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

