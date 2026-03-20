# ViberCampaignResponse


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**CampaignSchema**](CampaignSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.viber_campaign_response import ViberCampaignResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ViberCampaignResponse from a JSON string
viber_campaign_response_instance = ViberCampaignResponse.from_json(json)
# print the JSON string representation of the object
print(ViberCampaignResponse.to_json())

# convert the object into a dict
viber_campaign_response_dict = viber_campaign_response_instance.to_dict()
# create an instance of ViberCampaignResponse from a dict
viber_campaign_response_from_dict = ViberCampaignResponse.from_dict(viber_campaign_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

