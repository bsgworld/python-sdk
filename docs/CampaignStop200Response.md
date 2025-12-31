# CampaignStop200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**CampaignSchema**](CampaignSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.campaign_stop200_response import CampaignStop200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignStop200Response from a JSON string
campaign_stop200_response_instance = CampaignStop200Response.from_json(json)
# print the JSON string representation of the object
print(CampaignStop200Response.to_json())

# convert the object into a dict
campaign_stop200_response_dict = campaign_stop200_response_instance.to_dict()
# create an instance of CampaignStop200Response from a dict
campaign_stop200_response_from_dict = CampaignStop200Response.from_dict(campaign_stop200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

