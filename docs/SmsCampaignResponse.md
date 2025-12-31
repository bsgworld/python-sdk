# SmsCampaignResponse


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**CampaignSchema**](CampaignSchema.md) |  |  |

## Example

```python
from bsg_api.models.sms_campaign_response import SmsCampaignResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SmsCampaignResponse from a JSON string
sms_campaign_response_instance = SmsCampaignResponse.from_json(json)
# print the JSON string representation of the object
print(SmsCampaignResponse.to_json())

# convert the object into a dict
sms_campaign_response_dict = sms_campaign_response_instance.to_dict()
# create an instance of SmsCampaignResponse from a dict
sms_campaign_response_from_dict = SmsCampaignResponse.from_dict(sms_campaign_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

