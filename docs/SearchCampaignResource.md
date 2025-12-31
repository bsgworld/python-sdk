# SearchCampaignResource


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**List[CampaignSchema]**](CampaignSchema.md) | list of campaigns | [optional]  |
| **meta** | [**SearchCampaignResourceMeta**](SearchCampaignResourceMeta.md) |  | [optional]  |

## Example

```python
from bsg_api.models.search_campaign_resource import SearchCampaignResource

# TODO update the JSON string below
json = "{}"
# create an instance of SearchCampaignResource from a JSON string
search_campaign_resource_instance = SearchCampaignResource.from_json(json)
# print the JSON string representation of the object
print(SearchCampaignResource.to_json())

# convert the object into a dict
search_campaign_resource_dict = search_campaign_resource_instance.to_dict()
# create an instance of SearchCampaignResource from a dict
search_campaign_resource_from_dict = SearchCampaignResource.from_dict(search_campaign_resource_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

