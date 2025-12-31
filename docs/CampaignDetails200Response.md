# CampaignDetails200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**DetailCampaignSchema**](DetailCampaignSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.campaign_details200_response import CampaignDetails200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignDetails200Response from a JSON string
campaign_details200_response_instance = CampaignDetails200Response.from_json(json)
# print the JSON string representation of the object
print(CampaignDetails200Response.to_json())

# convert the object into a dict
campaign_details200_response_dict = campaign_details200_response_instance.to_dict()
# create an instance of CampaignDetails200Response from a dict
campaign_details200_response_from_dict = CampaignDetails200Response.from_dict(campaign_details200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

