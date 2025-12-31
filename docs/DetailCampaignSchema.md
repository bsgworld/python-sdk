# DetailCampaignSchema

Detailed campaign data including delivery stats, total message count and price

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **int** | campaign unique identifier | [optional]  |
| **name** | **str** | campaign auto generated name | [optional]  |
| **sender** | **str** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) | [optional]  |
| **status** | [**CampaignStatus**](CampaignStatus.md) |  | [optional]  |
| **type** | [**MessageType**](MessageType.md) |  | [optional]  |
| **started_at** | **datetime** | Start sending the messages at | [optional]  |
| **actual_start_at** | **datetime** | Real time when sending the messages starts | [optional]  |
| **finished_at** | **datetime** |  | [optional]  |
| **created_at** | **datetime** | Date when the item was created in the system ― set by the system automatically. Display format ― Y-m-d H:i:s | [optional]  |
| **statistics** | [**StatisticsData**](StatisticsData.md) |  | [optional]  |
| **alternative_channels** | [**DetailCampaignSchemaAlternativeChannels**](DetailCampaignSchemaAlternativeChannels.md) |  | [optional]  |
| **total_messages** | **int** | Total count of messages sent in campaign | [optional]  |
| **total_phones** | **int** | Total count if phone numbers in campaign | [optional]  |
| **total_price** | **float** | Total price of all the messages sent in campaign | [optional]  |
| **currency** | **str** | The currency code of the account. Specified according to the ISO-4217 standard | [optional]  |

## Example

```python
from bsg_api.models.detail_campaign_schema import DetailCampaignSchema

# TODO update the JSON string below
json = "{}"
# create an instance of DetailCampaignSchema from a JSON string
detail_campaign_schema_instance = DetailCampaignSchema.from_json(json)
# print the JSON string representation of the object
print(DetailCampaignSchema.to_json())

# convert the object into a dict
detail_campaign_schema_dict = detail_campaign_schema_instance.to_dict()
# create an instance of DetailCampaignSchema from a dict
detail_campaign_schema_from_dict = DetailCampaignSchema.from_dict(detail_campaign_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

