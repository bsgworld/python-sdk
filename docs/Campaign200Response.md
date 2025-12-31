# Campaign200Response


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**CampaignSchema**](CampaignSchema.md) |  | [optional]  |

## Example

```python
from bsg_api.models.campaign200_response import Campaign200Response

# TODO update the JSON string below
json = "{}"
# create an instance of Campaign200Response from a JSON string
campaign200_response_instance = Campaign200Response.from_json(json)
# print the JSON string representation of the object
print(Campaign200Response.to_json())

# convert the object into a dict
campaign200_response_dict = campaign200_response_instance.to_dict()
# create an instance of Campaign200Response from a dict
campaign200_response_from_dict = Campaign200Response.from_dict(campaign200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

