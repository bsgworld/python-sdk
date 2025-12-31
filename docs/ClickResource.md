# ClickResource


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **str** | click unique uuid | [optional]  |
| **browser_language** | **str** | Language of user browser | [optional]  |
| **country_code** | **str** | User country detected by geo ip | [optional]  |
| **is_human** | **bool** | We use some heuristics to determine is it real human or looks like bot | [optional]  |
| **is_unique** | **bool** | We use combination of ip address user-agent cookies and so on to account the same user just once | [optional]  |
| **http_status** | **int** | Status code returned by GET original link when redirecting the user | [optional]  |
| **http_method** | **str** | Http method used by user when click on short link | [optional]  |
| **created_at** | **datetime** | Date and time of click | [optional]  |
| **user_agent** | **str** | User-agent of first click | [optional]  |
| **client_ip** | **str** | Client IP address of first click | [optional]  |
| **browser** | **str** | User browser detected from user-agent | [optional]  |
| **referrer_url** | **str** | source page from witch user click on short link | [optional]  |
| **city** | **str** | User city detected by geo ip | [optional]  |
| **device_os** | **str** | User device operation system detected from user-agent | [optional]  |
| **short_link** | **str** | short link url that can be used to redirect to original link | [optional]  |
| **original_link** | **str** | Original link where to short link will redirect | [optional]  |
| **message_id** | **int** | message id for short links created as part of [sms campaign](#tag/Campaign-SMS) | [optional]  |
| **phone_number** | **int** | Phone number without leading plus. For short links created as part of [sms campaign](#tag/Campaign-SMS) | [optional]  |

## Example

```python
from bsg_api.models.click_resource import ClickResource

# TODO update the JSON string below
json = "{}"
# create an instance of ClickResource from a JSON string
click_resource_instance = ClickResource.from_json(json)
# print the JSON string representation of the object
print(ClickResource.to_json())

# convert the object into a dict
click_resource_dict = click_resource_instance.to_dict()
# create an instance of ClickResource from a dict
click_resource_from_dict = ClickResource.from_dict(click_resource_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

