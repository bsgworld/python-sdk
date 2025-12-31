# CampaignPrice422Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **str** | The given data was invalid. It can be one of the following:  - **The given data was invalid.** Detailed error is described in errors field. - **Tariff not found**  This error can occur when the tariff identifier is specified incorrectly or the specified tariff is not present in the system. Please ensure that you are using the correct tariff identifier and try again. For more information please visit the [account prices](https://app.bsg.world/prices/sms)   | [optional]  |
| **errors** | **List[object]** | errors | [optional]  |

## Example

```python
from bsg_api.models.campaign_price422_response import CampaignPrice422Response

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignPrice422Response from a JSON string
campaign_price422_response_instance = CampaignPrice422Response.from_json(json)
# print the JSON string representation of the object
print(CampaignPrice422Response.to_json())

# convert the object into a dict
campaign_price422_response_dict = campaign_price422_response_instance.to_dict()
# create an instance of CampaignPrice422Response from a dict
campaign_price422_response_from_dict = CampaignPrice422Response.from_dict(campaign_price422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

