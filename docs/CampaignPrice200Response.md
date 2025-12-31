# CampaignPrice200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price** | **float** | estimate campaign cost  **Please note:** price defined only as the response to create campaign or calculate price requests | [optional]  |
| **currency** | **str** | The currency code of the account. Specified according to the ISO-4217 standard | [optional]  |

## Example

```python
from bsg_api.models.campaign_price200_response import CampaignPrice200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignPrice200Response from a JSON string
campaign_price200_response_instance = CampaignPrice200Response.from_json(json)
# print the JSON string representation of the object
print(CampaignPrice200Response.to_json())

# convert the object into a dict
campaign_price200_response_dict = campaign_price200_response_instance.to_dict()
# create an instance of CampaignPrice200Response from a dict
campaign_price200_response_from_dict = CampaignPrice200Response.from_dict(campaign_price200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

