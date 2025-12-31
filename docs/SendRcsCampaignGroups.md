# SendRcsCampaignGroups


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **groups** | **List[int]** | An array of lists (list id) with contacts from the address book to which RCS campaigns are to be sent. id of the lists can be obtained: using the Get [lists API](#tag/Contact-List) in your account [Contact Book → Lists](https://app.bsg.world/addressbook/lists) |  |
| **sender** | **str** | The name of the agent used to send the rcs message |  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **options** | [**Options**](Options.md) |  |  |
| **alternative_channel** | [**SendRcsCampaignGroupsAlternativeChannel**](SendRcsCampaignGroupsAlternativeChannel.md) |  | [optional]  |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to True] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to True] |

## Example

```python
from bsg_api.models.send_rcs_campaign_groups import SendRcsCampaignGroups

# TODO update the JSON string below
json = "{}"
# create an instance of SendRcsCampaignGroups from a JSON string
send_rcs_campaign_groups_instance = SendRcsCampaignGroups.from_json(json)
# print the JSON string representation of the object
print(SendRcsCampaignGroups.to_json())

# convert the object into a dict
send_rcs_campaign_groups_dict = send_rcs_campaign_groups_instance.to_dict()
# create an instance of SendRcsCampaignGroups from a dict
send_rcs_campaign_groups_from_dict = SendRcsCampaignGroups.from_dict(send_rcs_campaign_groups_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

