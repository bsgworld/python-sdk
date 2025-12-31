# CampaignStop422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | Invalid campaign status  The campaign must be in one of following status to be able to stop: \&quot;scheduled\&quot;, \&quot;sending\&quot;, \&quot;paused\&quot;, \&quot;moderation\&quot; | [optional]  |
| **errors** | **List[object]** | errors | [optional]  |

## Example

```python
from bsg_api.models.campaign_stop422_response import CampaignStop422Response

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignStop422Response from a JSON string
campaign_stop422_response_instance = CampaignStop422Response.from_json(json)
# print the JSON string representation of the object
print(CampaignStop422Response.to_json())

# convert the object into a dict
campaign_stop422_response_dict = campaign_stop422_response_instance.to_dict()
# create an instance of CampaignStop422Response from a dict
campaign_stop422_response_from_dict = CampaignStop422Response.from_dict(campaign_stop422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

