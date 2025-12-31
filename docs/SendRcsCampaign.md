# SendRcsCampaign


## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **phones** | [**List[Phone]**](Phone.md) | The list of objects containing information about the mobile phone number (number) and (reference_id) to send a message to |  |
| **sender** | **str** | The name of the agent used to send the rcs message |  |
| **options** | [**Options**](Options.md) |  |  |
| **alternative_channel** | [**AlternativeChannel**](AlternativeChannel.md) |  | [optional]  |
| **start_at** | **datetime** | Start sending the messages at | [optional]  |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional]  |
| **validity_seconds** | **int** | Message validity period in seconds. After this period expires, the message will be in **EXPIRED** status or will be redirected to the SMS channel if it was specified in the request | [optional]  |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to True] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to True] |

## Example

```python
from bsg_api.models.send_rcs_campaign import SendRcsCampaign

# TODO update the JSON string below
json = "{}"
# create an instance of SendRcsCampaign from a JSON string
send_rcs_campaign_instance = SendRcsCampaign.from_json(json)
# print the JSON string representation of the object
print(SendRcsCampaign.to_json())

# convert the object into a dict
send_rcs_campaign_dict = send_rcs_campaign_instance.to_dict()
# create an instance of SendRcsCampaign from a dict
send_rcs_campaign_from_dict = SendRcsCampaign.from_dict(send_rcs_campaign_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

