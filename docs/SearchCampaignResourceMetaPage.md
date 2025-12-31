# SearchCampaignResourceMetaPage


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **int** | Total items count at all of the pages | [optional]  |
| **limit** | **int** |  | [optional]  |
| **offset** | **int** |  | [optional]  |

## Example

```python
from bsg_api.models.search_campaign_resource_meta_page import SearchCampaignResourceMetaPage

# TODO update the JSON string below
json = "{}"
# create an instance of SearchCampaignResourceMetaPage from a JSON string
search_campaign_resource_meta_page_instance = SearchCampaignResourceMetaPage.from_json(json)
# print the JSON string representation of the object
print(SearchCampaignResourceMetaPage.to_json())

# convert the object into a dict
search_campaign_resource_meta_page_dict = search_campaign_resource_meta_page_instance.to_dict()
# create an instance of SearchCampaignResourceMetaPage from a dict
search_campaign_resource_meta_page_from_dict = SearchCampaignResourceMetaPage.from_dict(search_campaign_resource_meta_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

