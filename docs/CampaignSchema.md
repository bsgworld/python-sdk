# CampaignSchema

Main campaign properties

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | campaign unique identifier | [optional]  |
| **name** | **str** | campaign auto generated name | [optional]  |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) | [optional]  |
| **status** | [**CampaignStatus**](CampaignStatus.md) |  | [optional]  |
| **message_type** | [**MessageType**](MessageType.md) |  | [optional]  |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **real_start_at** | **datetime** | Real time when sending the messages starts | [optional]  |
| **finished_at** | **datetime** |  | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **statistics** | [**StatisticsShort**](StatisticsShort.md) |  | [optional]  |
| **calculated_price** | **float** | estimate campaign cost  **Please note:** price defined only as the response to create campaign or calculate price requests | [optional]  |
| **currency** | **str** | The currency code of the account. Specified according to the ISO-4217 standard | [optional]  |

## Example

```python
from bsg_api.models.campaign_schema import CampaignSchema

# TODO update the JSON string below
json = "{}"
# create an instance of CampaignSchema from a JSON string
campaign_schema_instance = CampaignSchema.from_json(json)
# print the JSON string representation of the object
print(CampaignSchema.to_json())

# convert the object into a dict
campaign_schema_dict = campaign_schema_instance.to_dict()
# create an instance of CampaignSchema from a dict
campaign_schema_from_dict = CampaignSchema.from_dict(campaign_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

