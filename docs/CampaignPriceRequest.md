# CampaignPriceRequest


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) |  |
| **text** | **str** | Message text to send |  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **groups** | **List[int]** |  | [optional]  |
| **messages** | [**List[CampaignPriceRequestMessagesItem]**](CampaignPriceRequestMessagesItem.md) |  | [optional]  |

## Example

```python
from bsg_api.models.campaign_price_request import CampaignPriceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignPriceRequest from a JSON string
campaign_price_request_instance = CampaignPriceRequest.from_json(json)
# print the JSON string representation of the object
print(CampaignPriceRequest.to_json())

# convert the object into a dict
campaign_price_request_dict = campaign_price_request_instance.to_dict()
# create an instance of CampaignPriceRequest from a dict
campaign_price_request_from_dict = CampaignPriceRequest.from_dict(campaign_price_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

