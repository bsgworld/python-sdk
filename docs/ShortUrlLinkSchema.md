# ShortUrlLinkSchema

Short Link object

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | short link unique id | [optional]  |
| **status** | [**ShortLinkStatus**](ShortLinkStatus.md) |  | [optional]  |
| **name** | **str** | Name of short link. like a comment | [optional]  |
| **slug** | **str** | part of short link after domain | [optional]  |
| **campaign_id** | **int** | campaign ID if short link is part of sms campaign.  Campaign allow send messages to all the leads with different short link for each lead that follows to the same original link | [optional]  |
| **message_id** | **int** | message id for short links created as part of [sms campaign](#tag/Campaign-SMS) | [optional]  |
| **init_deleted_at** | **datetime** | Date and time when short link was deactivated | [optional]  |
| **created_at** | **datetime** | Date and time when short link was created | [optional]  |
| **short_link** | **str** | short link url that can be used to redirect to original link | [optional]  |
| **original_link** | **str** | Original link where to short link will redirect | [optional]  |
| **can_restore** | **bool** | For link marked as deleted it can be restored a few time if can_restore&#x3D;true | [optional] [default to True] |
| **count_clicks** | **int** | Number of clicks on a short link  *Please note: count of clicks updated with some latency* | [optional]  |
| **count_human_clicks** | **int** | Number of clicks on a short link looks like human  We use some heuristics to determine is it real human or looks like bot | [optional]  |
| **count_unique_clicks** | **int** | Number of unique clicks on a short link  We use combination of ip address user-agent cookies and so on to account the same user just once | [optional]  |

## Example

```python
from bsg_api.models.short_url_link_schema import ShortUrlLinkSchema

# TODO update the JSON string below
json = "{}"
# create an instance of ShortUrlLinkSchema from a JSON string
short_url_link_schema_instance = ShortUrlLinkSchema.from_json(json)
# print the JSON string representation of the object
print(ShortUrlLinkSchema.to_json())

# convert the object into a dict
short_url_link_schema_dict = short_url_link_schema_instance.to_dict()
# create an instance of ShortUrlLinkSchema from a dict
short_url_link_schema_from_dict = ShortUrlLinkSchema.from_dict(short_url_link_schema_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

