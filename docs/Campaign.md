# Campaign


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to True] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to True] |
| **recipients** | [**Recipients**](Recipients.md) |  |  |
| **channels** | **List[str]** |  |  |
| **rcs** | [**Rcs**](Rcs.md) |  | [optional]  |
| **viber** | [**Viber**](Viber.md) |  | [optional]  |
| **sms** | [**Sms**](Sms.md) |  | [optional]  |
| **voice** | [**Voice**](Voice.md) |  | [optional]  |
| **telegram** | [**Telegram**](Telegram.md) |  | [optional]  |
| **dry_run** | **bool** | Allows you to check the validity of the request without actual campaign sending | [optional] [default to False] |

## Example

```python
from bsg_api.models.campaign import Campaign

# TODO update the JSON string below
json = "{}"
# create an instance of Campaign from a JSON string
campaign_instance = Campaign.from_json(json)
# print the JSON string representation of the object
print(Campaign.to_json())

# convert the object into a dict
campaign_dict = campaign_instance.to_dict()
# create an instance of Campaign from a dict
campaign_from_dict = Campaign.from_dict(campaign_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

