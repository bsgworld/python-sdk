# ShortUrlsLinkStatisticData


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **count_clicks** | **int** | Number of clicks on a short link  *Please note: count of clicks updated with some latency* | [optional]  |
| **short_link** | **str** | short link url that can be used to redirect to original link | [optional]  |
| **click_date** | **datetime** | Date of first click | [optional]  |
| **click_id** | **str** | click unique uuid | [optional]  |
| **user_agent** | **str** | User-agent of first click | [optional]  |
| **client_ip** | **str** | Client IP address of first click | [optional]  |
| **original_link** | **str** | Original link where to short link will redirect | [optional]  |
| **phone** | **int** | Phone number without leading plus. For short links created as part of [sms campaign](#tag/Campaign-SMS) | [optional]  |
| **message_id** | **int** | message id for short links created as part of [sms campaign](#tag/Campaign-SMS) | [optional]  |
| **campaign_id** | **int** | campaign ID if short link is part of sms campaign.  Campaign allow send messages to all the leads with different short link for each lead that follows to the same original link | [optional]  |
| **is_human** | **bool** | We use some heuristics to determine is it real human or looks like bot | [optional]  |

## Example

```python
from bsg_api.models.short_urls_link_statistic_data import ShortUrlsLinkStatisticData

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlsLinkStatisticData from a JSON string
short_urls_link_statistic_data_instance = ShortUrlsLinkStatisticData.from_json(json)
# print the JSON string representation of the object
print(ShortUrlsLinkStatisticData.to_json())

# convert the object into a dict
short_urls_link_statistic_data_dict = short_urls_link_statistic_data_instance.to_dict()
# create an instance of ShortUrlsLinkStatisticData from a dict
short_urls_link_statistic_data_from_dict = ShortUrlsLinkStatisticData.from_dict(short_urls_link_statistic_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

