# SearchCampaignResourceMeta

Total count of items, current offset and page limit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | [**SearchCampaignResourceMetaPage**](SearchCampaignResourceMetaPage.md) |  | [optional]  |

## Example

```python
from bsg_api.models.search_campaign_resource_meta import SearchCampaignResourceMeta

# TODO update the JSON string below
json = "{}"
# create an instance of SearchCampaignResourceMeta from a JSON string
search_campaign_resource_meta_instance = SearchCampaignResourceMeta.from_json(json)
# print the JSON string representation of the object
print(SearchCampaignResourceMeta.to_json())

# convert the object into a dict
search_campaign_resource_meta_dict = search_campaign_resource_meta_instance.to_dict()
# create an instance of SearchCampaignResourceMeta from a dict
search_campaign_resource_meta_from_dict = SearchCampaignResourceMeta.from_dict(search_campaign_resource_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

