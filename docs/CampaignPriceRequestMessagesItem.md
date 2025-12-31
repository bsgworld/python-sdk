# CampaignPriceRequestMessagesItem


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phone** | **int** | Phone number without leading plus, just digits | [optional]  |

## Example

```python
from bsg_api.models.campaign_price_request_messages_item import CampaignPriceRequestMessagesItem

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignPriceRequestMessagesItem from a JSON string
campaign_price_request_messages_item_instance = CampaignPriceRequestMessagesItem.from_json(json)
# print the JSON string representation of the object
print(CampaignPriceRequestMessagesItem.to_json())

# convert the object into a dict
campaign_price_request_messages_item_dict = campaign_price_request_messages_item_instance.to_dict()
# create an instance of CampaignPriceRequestMessagesItem from a dict
campaign_price_request_messages_item_from_dict = CampaignPriceRequestMessagesItem.from_dict(campaign_price_request_messages_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

